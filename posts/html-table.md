---
title: 'HTML Table'
date: '2017-12-05'
readTime: '5'
---

When we want to build a HTMl table, we first need to think what elements we need to have with a table? 

- Title
- Headers
- Rows
- Columns
- Borders or styles
- Data for the values

Some of these items have some HTML tags that transfer over but we just need to learn the syntax. 

When we want to create a Table we would use the Table tags 

```html
<table>
</table>
```

If we want to title then we would do a cation tag with the title you want.

```html
<table>
  <caption>People</caption>
</table>
```

The next part is going to be optional and more for organization and you could use it without it and it would still work. Which is the thead, tbody, tfoot to group together elements in the header, body and footer of the table.

```html
<table>
  <caption>People</caption>
  <thead>
  </thead>
  <tbody>
  </tbody>
  <tfoot>
  </tfoot>
</table>
```

For the header you would need the th tag to define the labels of each columns. 

<table>
  <caption>People</caption>
  <thead>
    <th>
      First Name
    </th>
    <th>
      Last Name
    </th>
    <th>
      Age
    </th>
    <th>
      Email
    </th>
  </thead>
  <tbody>
  </tbody>
  <tfoot>
  </tfoot>
</table>
```

It is better to be putting elements in rows since tables are made up of rows and columns and we can do the tr tags for the rows. There is a col and colgroup tags to define columns but not a lot of people use it so we will omit it. 

```html
<table>
  <caption>People</caption>
  <thead>
    <tr>
      <th>
        First Name
      </th>
      <th>
        Last Name
      </th>
      <th>
        Age
      </th>
      <th>
        Email
      </th>
    </tr>
  </thead>
  <tbody>
  </tbody>
  <tfoot>
  </tfoot>
</table>
```

Next is for the data of the values of the columns, and for each entry we will be using tr to define the rows and td to define the data.

```html
<table>
  <caption>People</caption>
  <thead>
    <tr>
      <th>
        First Name
      </th>
      <th>
        Last Name
      </th>
      <th>
        Age
      </th>
      <th>
        Email
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Bob</td>
      <td>Smith</td>
      <td>34</td>
      <td>bob@email.com</td>
    </tr>
    <tr>
      <td>Jill</td>
      <td>Jones</td>
      <td>24</td>
      <td>jill@email.com</td>
    </tr>
    <tr>
      <td>Craig</td>
      <td>Maybel</td>
      <td>44</td>
      <td>Craig@email.com</td>
    </tr>
  </tbody>
  <tfoot>
  </tfoot>
</table>
```

Now your table is complete, but if you look at it in your browser there isn't much to look at. That is where styles will come in. So we wont go too much into styling but you can style the borders, the rows and columns and all aspects of the table based off of how you want it. We are just going to add borders for now and then you can come back and make it great!

styles.css
```css
table, th, td {
  border: 1px solid black;
}
```
