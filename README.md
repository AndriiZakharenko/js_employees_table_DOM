### Task: Employees table

1. Implement table sorting by clicking on the title (in two directions).
2. When user clicks on a row, it should become selected.
3. Write a script to add a form to the document. Form allows users to add new employees to the spreadsheet.
4. Show notification if form data is invalid (use notification from the previous tasks).
5. Implement editing of table cells by double-clicking on it. (optional)

Start table:
![Preview](./src/images/preview.png)

##### Implement table sorting by clicking on the title (in two directions)
- When users clicks on one of the table headers, table should be sorted in ASC order, the second click sorts it in DESC order.
- When users click on a new title, always sort in ASC order.

##### When user clicks on a row, it should become selected.
- Use 'active' class for table row to indicate it is selected.
- Only one line can be selected at a time.

##### Write a script to add a form to the document. Form allows users to add new employees to the spreadsheet.
- The form should have class `new-employee-form` (to apply correct styles).
- The form should have 4 inputs, 1 select and submit button.
- Put inputs inside labels:
```html
<label>Name: <input name="name" type="text"></label>
```
- Add qa attributes for each input field:
```
 data-qa="name" 
 data-qa="position" 
 data-qa="office" 
 data-qa="age" 
 data-qa="salary" 
```
- Select should have 6 options: `Tokyo`, `Singapore`, `London`, `New York`, `Edinburgh`, `San Francisco`.
- Use texts for labels and buttons from the screenshot below.
- Age and salary inputs should have a number type. Don't forget to convert the string from salary input to correct value like in the table.
- Click on `Save to table` should add a new employee to the table.
- All fields are required.

##### Show notification if form data is invalid.
- Click on `Save to table` should run validation for form inputs. If data is valid, add a new employee to the table.
- If `Name` value has less than 4 letters, show error notification.
- If `Age` value is less than 18 or more than 90 show error notification.
- If a new employee is successfully added to the table, show success notification.
- Notification titles and descriptions are up to you.
- Add qa attribute for notification: `data-qa="notification"` and class `error`/`success` depending on the result.

##### Implement editing of table cells by double-clicking on it (optional). 
- Double click on the cell of the table, should remove text, and append input with `cell-input` class.
- The input value should contain replaced by input text.
- Only one cell can be edited at the time.
- On blur save changes to table cell. Remove input and set new text.
- On 'Enter' keypress, save changes to the table cell. Remove input and set new text in the table cell.
- If an input is empty on submitting return initial value.

Expected result of your code:
![Result](./src/images/result.png)

## Demo Links

- [DEMO LINK](https://AndriiZakharenko.github.io/js_employees_table_DOM/)
