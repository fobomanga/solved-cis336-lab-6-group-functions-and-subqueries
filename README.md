Download Link: https://assignmentchef.com/product/solved-cis336-lab-6-group-functions-and-subqueries
<br>
<header class="entry-header">

 <p class="entry-title">Lab 6 will introduce the concept of group functions and subqueries to meet more complex report requirements. This lab may be completed using either DeVry’s Omnymbus EDUPE-APP lab environment, or a local copy of the MySQL database running on your own computer using the OM database tables. The lab will utilize a set of tables that are represented by the ERD (OM_ERD.docx) and are created and populated by the script file (create_OM_db.sql). Follow the instructions in the file CreateOMTables.docx to create your database, tables, and data.

</header>

5/5 - (4 votes)

A few IMPORTANT things to note if using EDUPE MySQL:**There can be NO SPACES in alias names given to a column. For example:Select unit_price as “Retail Price “ from items; –this does NOT work in EDUPE MySQL.Any of the following WILL WORK:

**Any calculated fields MUST be given an alias (and note above NO SPACES in alias). For example:select unit_price * 2 from items; –this does NOT work in EDUPE MySQLThis will work:

<strong>Deliverables</strong>Lab Report (Answer Sheet) containing both the student-created SQL command(s) for each exercise, and the output showing the results obtained. Be sure your name is on the file.

<strong>LAB STEPS:</strong> Complete each of the exercises below.

<ol type="1">

 <li>Write a query to determine the total number of items on each order. Display the order_id and the total with a heading of TotalItems (note no spaces). Filter to only display information for order_id of 600 or higher.</li>

 <li>Re-do query 1 but filter to only show those orders with more than 2 items ordered. Sort by the number of items ordered, lowest to highest.</li>

 <li>The order_details table has a quantity for each item ordered. Show the total amount charged for each item on the order (quantity times price). Display order_id, the item id, the unit price, the quantity times price of the item labeled as “Itemtotal” (note NO spaces). Sort by order id and filter to only display those order ids between 400 and 700.</li>

 <li>Write a query to display the total amount for each order: show the order id and total. Sort by descending order on the total and only display orders with a total of $40 or more.</li>

 <li>Re-do query 4 but show the customer name for each order (formatted as a single field with heading of Customer) along with the city, order id and total. Filter to only display customers that live in California. Sort by city.</li>

 <li>Display the total amount of sales per item. Show title, total quantity sold with a heading of Quantity, total sales with a heading of “TotalSales” (not NO space). Sort by highest to lowest total.</li>

 <li>Display the total sales for each customer: show customer name (as single field) with a heading of Cutomer and total. Sort lowest to highest total. Filter to only display customers with $50 or more in total orders.</li>

 <li>Use subqueries to determine which (artist) had the item ordered in highest quantity on an order? First determine the highest quantity on any order, then determine the item number associated with it, then display the artist.</li>

 <li>Display the total sales by artist: show artist name, total. Sort highest to lowest.</li>

 <li>USE A SUBQUERY to Increase price of all items by ‘No Rest for the Weary’ by 10%. If working in MySQl you will need to disable safe mode. Show prices before and after. Rollback after.</li>

 <li>USE A SUBQUERY to display names of customers that have unshipped orders.</li>

 <li>Display the total amount of sales made to customers in NY</li>

 <li>USE A SUBQUERY to list the items (title and artist) of items that have never been ordered</li>

 <li>Show the order history for Samuel Jacobsen. Display the order id, order date, ship date, and total.</li>

 <li>Show the total amount of sales per sales rep. Display the employee name as a single field along with the total sales, sorted by highest to lowest sales.</li>

</ol>

This is the end of Lab 6.

<table border="0" cellspacing="0" cellpadding="0">

 <tbody>

  <tr>

   <td class="gutter"></td>

   <td class="code"></td>

  </tr>

 </tbody>

</table>

1

2

3

4

<code class="php plain">Select unit_price </code><code class="php keyword">as</code> <code class="php plain">“RetailPrice” from items;</code>

<code class="php plain">Select unit_price </code><code class="php keyword">as</code> <code class="php plain">“Retail_Price” from items;</code>

<code class="php plain">Select unit_price </code><code class="php keyword">as</code> <code class="php plain">Retail_Price from items;</code>

<code class="php plain">Select unit_price </code><code class="php keyword">as</code> <code class="php plain">RetailPrice from items;</code>

<table border="0" cellspacing="0" cellpadding="0">

 <tbody>

  <tr>

   <td class="gutter"></td>

   <td class="code"></td>

  </tr>

 </tbody>

</table>

1