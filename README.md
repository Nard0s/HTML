# Tables Using HTML 

Table has an external border, header rows and header cell, body rows and its cells and it could have also a footer row. To make an HTML table, we need a _table_ element that wrap all the rows and the rows wrap all the data cells.


## Basic HTML Table Syntax

The basic structure of an HTML table includes the following elements:

- `<table>`: Wraps the entire table.
- `<tr>`: Represents a table row.
- `<th>`: Represents a header cell (bold and centered by default).
- `<td>`: Represents a data cell.

### syntax:

```html
<table>
  <!-- first row -->
  <tr>
    <th>Header 1</th>
    <th>Header 2</th>
    <th>Header 3</th>
  </tr>
  <!-- Second row -->
  <tr>
    <td>Row 1, Col 1</td>
    <td>Row 1, Col 2</td>
    <td>Row 1, Col 3</td>
  </tr>
  <!-- Third row -->
  <tr>
    <td>Row 2, Col 1</td>
    <td>Row 2, Col 2</td>
    <td>Row 2, Col 3</td>
  </tr>
</table>

```
### Example

```html
<table>
  <tr>
    <td>Name</td>
    <td>Gender</td>
    <td>Country</td>
  </tr>
  <tr>
    <td>Nardos</td>
    <td>Female</td>
    <td>Ethopia</td>
  </tr>
</table>
```



# `<input>` Tag and Its Types

The `<input>` element in HTML is used to create interactive controls for web forms. It allows users to input data. The `type` attribute specifies the type of input field to display.

Below are the common types of `<input>` and their uses, along with examples:

---

## 1. Text Input
Used for single-line text input.

```html
<input type="text" name="username" placeholder="Enter your username">
```

## 2. Password Input
Used for entering passwords. The characters are obscured.

```html
<input type="password" name="password" placeholder="Enter your password">
```

## 3. Email Input
Used for email addresses. It validates the input as a properly formatted email.
```html
<input type="email" name="email" placeholder="Enter your email">
```
## 4. Number Input
Used for numeric inputs. You can specify min, max, and step values.
```html
<input type="number" name="age" min="1" max="100" step="1">
```
## 5. Date Input
Used to select a date from a calendar.

```html
<input type="date" name="birthdate">
```
## 6. Checkbox Input
Used for selecting one or more options.
```html
<label>
  <input type="checkbox" name="subscribe" value="newsletter"> Subscribe to newsletter
</label>
```
## 7 Radio Button input
used for selecting a single option from multiple choices.
```html
<label>
  <input type="radio" name="gender" value="male"> Male
</label>
<label>
  <input type="radio" name="gender" value="female"> Female
</label>
```
## 8. File Input
Used for uploading files.
```html
<input type="file" name="profilePicture">
```
## 9. Color Input
Used for selecting a color from a color picker.
```html
<input type="color" name="favoriteColor">
```
## 10. Submit Button
used to submit a form.
```html
<input type="submit" value="Submit">
```
### In addition learn more about in [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)







# HTML Form Elements

HTML forms are used to collect user input. They contain various form elements like text fields, checkboxes, radio buttons, and more. Below is a detailed explanation of the most common form elements with examples.

---

## 1. `<form>` Element
The `<form>` tag defines an HTML form and serves as a container for input elements. It requires attributes like `action` (where to send data) and `method` (HTTP method to use).

```html
<form action="/submit" method="post">
  <!-- Form elements go here -->
</form>
```

The `action` and `method` attributes are key components of an HTML `<form>` element, determining where and how form data is submitted. Here's an explanation of each:
### 1. The action Attribute
The `action` attribute specifies the URL where the form data should be sent once the form is submitted.

```html
<form action="URL">
  <!-- Form content -->
</form>
```
#### URL can be an absolute or relative path:
- ***Absolute URL***: The full path to a server (`e.g., https://example.com/submit`).

- ***Relative URL***: A path relative to the current page (e.g., `/submit`).

### Example
```html
<form action="https://example.com/submit" method="post">
  <input type="text" name="username" placeholder="Enter your name">
  <input type="submit" value="Submit">
</form>
```
When the user submits this form, the data is sent to `https://example.com/submit`.
### 2. The method Attribute
The method attribute specifies the HTTP method used to send the form data to the server.

Common Values:

***1.`GET`:***

- Appends form data to the URL as query parameters.
- Data is visible in the browser's address bar.
- Suitable for non-sensitive data or bookmarking.

### Example:
```html
<form action="/search" method="get">
  <input type="text" name="q" placeholder="Search">
  <input type="submit" value="Search">
</form>
```
Submitting the form might result in a URL like:
`https://example.com/search?q=search-term.`

***2.`POST`***:

- Sends form data in the HTTP request body.
- Data is not visible in the URL.
- Suitable for sensitive or large amounts of data

### Example:
```html
