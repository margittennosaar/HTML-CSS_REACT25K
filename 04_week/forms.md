# HTML Forms and Input elements

## Form Structure
A basic form consists of a `<form>` element that contains input fields and a submit button.

### Example of a Simple Form

```html
<form action="/submit" method="POST">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required>

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>

  <button type="submit">Submit</button>
</form>
```

### **Key attributes in forms**
- **`action`** → Where to send the form data.
- **`method`** → `GET` (visible in URL) or `POST` (secure for sensitive data).
- **`name`** → Identifies the input when the form is submitted.
- **`id`** → Links the input to its `<label>`.
- **`required`** → Ensures the field must be filled before submission.


## Semantic form elements

Using semantic HTML makes forms more readable and accessible.

### **Key semantic elements**
| Element      | Description                      |
| ------------ | -------------------------------- |
| `<form>`     | Defines a form section           |
| `<label>`    | Describes an input field         |
| `<input>`    | Standard input field             |
| `<textarea>` | Multi-line text input            |
| `<select>`   | Dropdown menu                    |
| `<option>`   | Individual items in a `<select>` |
| `<fieldset>` | Groups related fields            |
| `<legend>`   | Title for a `<fieldset>`         |
| `<button>`   | Form submission button           |

```html
<form>
  <fieldset>
    <legend>Personal Information</legend>
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>

    <label for="message">Message:</label>
    <textarea id="message" name="message" rows="4" cols="30"></textarea>
  </fieldset>

  <button type="submit">Submit</button>
</form>
```

## Common input types
| Input Type | Description                     |
| ---------- | ------------------------------- |
| `text`     | Basic text input                |
| `email`    | Requires a valid email format   |
| `password` | Hides input characters          |
| `number`   | Only allows numbers             |
| `tel`      | Accepts phone numbers           |
| `date`     | Date picker                     |
| `checkbox` | Allows multiple selections      |
| `radio`    | Selects one option from a group |
| `file`     | Uploads a file                  |
| `submit`   | Submits the form                |

### Example with different input types

```html
<form>
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>

  <label for="age">Age:</label>
  <input type="number" id="age" name="age" min="18">

  <label for="dob">Date of Birth:</label>
  <input type="date" id="dob" name="dob">

  <label>Choose an option:</label>
  <input type="radio" id="option1" name="choice" value="1"> Option 1
  <input type="radio" id="option2" name="choice" value="2"> Option 2

  <button type="submit">Submit</button>
</form>
```

## Best Practices for Forms
- Use **semantic elements** like `<label>` to improve accessibility.  
- Add **`required`** and **`placeholder`** attributes for user guidance.  
- Use **`fieldset`** and **`legend`** to group related fields.  
- Ensure **labels and inputs are properly linked** using the `for` attribute.  
- Provide **helpful error messages** when validation fails.  


