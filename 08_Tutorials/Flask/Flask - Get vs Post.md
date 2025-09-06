---
tags: [flask, http, get, post, methods]
---

# GET vs POST

When building [[Flask - Overview|Flask]] routes, you’ll often choose between **GET** and **POST** request methods. These are two of the most common **HTTP methods** browsers use to talk to your server.

---

## GET

- **Purpose**: Fetch data from the server.
- **How it looks**: Data is sent in the **URL** (query string) - http://example.com/search?term=flask
- **Visible in browser**: Parameters appear in the address bar.
- **Idempotent** (same request does not change state).
- Good for:
- Search queries
- Navigation
- Bookmarkable/sharable links

### Example (Flask)
```python
from flask import request

@app.route("/search")
def search():
  term = request.args.get("term")  # from URL query
  return f"You searched for: {term}"
  ```

Open in browser:  
`http://127.0.0.1:5000/search?term=python`

----------------------------------------------------------------------------------------------------
## POST

- **Purpose**: Send data to the server (create/update something).
- **How it looks**: Data is sent in the **request body**, not in the URL.
- **Hidden from the URL**: Better for sensitive or large inputs.
- **Not idempotent** (repeated requests can change server state).

- Good for:
    - Forms that change data (logins, submissions)
    - Sending hidden or sensitive fields
    - Uploads
        

### Example (Flask)

``` python
from flask import request, render_template  

@app.route("/submit", methods=["GET", "POST"]) 
def submit():
    if request.method == "POST":         
    name = request.form.get("name")         
    return f"Welcome, {name}!"     
    return render_template("form.html")
    
```

HTML form (`templates/form.html`):

<form method="POST">
  <input name="name" placeholder="Enter your name">
  <button type="submit">Submit</button>
</form>

---

## Quick Comparison

| Aspect          | GET                               | POST                      |
| --------------- | --------------------------------- | ------------------------- |
| Data location   | In URL query string               | In request body           |
| Visible?        | Yes (in address bar & logs)       | No (not in address bar)   |
| Length limit    | Limited (URL length restrictions) | Larger, can handle files  |
| Safe/idempotent | Yes (doesn’t change server state) | No (changes server state) |
| Use case        | Reading/fetching                  | Writing/submitting        |

----

## In Obsidian Hub

- This note links back to [[Flask Hub]].