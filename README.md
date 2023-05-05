Download Link: https://assignmentchef.com/product/solved-dbs301-assignment-2-database-normalization-and-erd
<br>
Print ERD and Normalization solution and hand in to the teacher in the class. One document per group is required. I will go through it in the class. If any group member is not present will receive 1% penalty. In each problem Normalization is 15 marks each and ERD is 10 marks each.




<h1>Problem 1:  travel expense database design</h1>

See the expense report form below. Design the database to support it and bring the tables to

3NF by answering the following questions.

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2020/01/224-1.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2020/01/224-1.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>

<ol>

 <li>Based on the expense report, start with the following original table schema:</li>

</ol>

<strong>Expense </strong><strong>(<u>StatementNumber</u>, EmployeeID, Name, Title, Email, Department, Manager, StartDateOfTrip, Nbdays, TripPurpose, <u>ExpenseLineNumber</u>, ExpenseDate, Account, Description, Vendor, Category, PaymentMethod, Amount)</strong><strong>. </strong>Consider (StatementNumber, ExpenseLineNumber) as PK. Draw the dependency diagram. Make sure you label the transitive and/or partial dependencies.

Account refers to a general ledger (GL) account created to hold expense information. Every single type of expense has a GL code or account that is composed of department and type of expense. For instance, an employee working in the IT department (has id 10) has to enter the airplane expense (category T with ID 100) in the first line of the expense report, the GL account is then 10100.

<strong>Definition</strong>:  A <a href="http://www.investopedia.com/terms/g/generalledger.asp">general ledger</a> is a complete record of financial transactions over the life of a company. The ledger holds account information that is needed to prepare financial statements, and includes accounts for assets, liabilities, owners’ equity, revenues and expenses.

<ol>

 <li>Write the relational schemas and create a set of dependency diagrams that meet 3NF requirements. Rename attributes to meet the naming conventions, and create new entities and add attributes as necessary.</li>

 <li>Draw the Crow’s Foot ERD. You can use VISIO, Word, etc.</li>

</ol>

<h1>Problem 2: Bus stations database</h1>

Have a look at the Bus/Train route/line schedule <a href="http://www.gotransit.com/timetables/en/schedules/schedules_window.aspx?tableid=38&amp;dir=N&amp;date=2016-06-29&amp;parentid=1">example</a> for

Bolton/Malton/North York route provided on gotransit.com.  Use the following schedule table schema as a startup to answer the following questions.




<table width="696">

 <tbody>

  <tr>

   <td width="78"><strong>routeNum</strong></td>

   <td width="54"><strong>stopId</strong></td>

   <td width="84"><strong>StopName</strong></td>

   <td width="72"><strong>StopType</strong></td>

   <td width="96"><strong>SeqOnRoute</strong><strong>//SEQUENCE ON ROUTE</strong></td>

   <td width="102"><strong>Depaturetime</strong></td>

   <td width="144"><strong>stopLocation</strong></td>

   <td width="66"><strong>status</strong></td>

  </tr>

  <tr>

   <td width="78"><strong>31</strong></td>

   <td width="54">101</td>

   <td width="84">Union Station Bus Terminal</td>

   <td width="72">B</td>

   <td width="96">1</td>

   <td width="102">09 00</td>

   <td width="144">141 Bay Street, Toronto, ON</td>

   <td width="66">On time</td>

  </tr>

  <tr>

   <td width="78"><strong>31</strong></td>

   <td width="54">102</td>

   <td width="84">York Mills Bus Terminal</td>

   <td width="72">B</td>

   <td width="96">2</td>

   <td width="102">09 00</td>

   <td width="144">4023 Yonge St., North York, ON</td>

   <td width="66">On time</td>

  </tr>

  <tr>

   <td width="78"><strong>31</strong></td>

   <td width="54">103</td>

   <td width="84">Yorkdale Bus Terminal</td>

   <td width="72">B</td>

   <td width="96">3</td>

   <td width="102">09 00</td>

   <td width="144">1 Yorkdale Road, North York, ON</td>

   <td width="66">On time</td>

  </tr>

  <tr>

   <td width="78"><strong>31</strong></td>

   <td width="54">104</td>

   <td width="84">Bloor GO</td>

   <td width="72">T</td>

   <td width="96">4</td>

   <td width="102">09 00</td>

   <td width="144">1456 Bloor Street West, Toronto, ON</td>

   <td width="66">On time</td>

  </tr>

  <tr>

   <td width="78"><strong>31</strong></td>

   <td width="54">105</td>

   <td width="84">Weston GO</td>

   <td width="72">T</td>

   <td width="96">5</td>

   <td width="102">09 00</td>

   <td width="144">1865 Weston Road, Etobicoke, ON</td>

   <td width="66">On time</td>

  </tr>

  <tr>

   <td width="78"><strong>31</strong></td>

   <td width="54">106</td>

   <td width="84">Etobicoke North GO</td>

   <td width="72">TB</td>

   <td width="96">6</td>

   <td width="102">09 00</td>

   <td width="144">1949 Kipling Ave., Etobicoke, ON</td>

   <td width="66">On time</td>

  </tr>

  <tr>

   <td width="78"><strong>31</strong></td>

   <td width="54">107</td>

   <td width="84">Malton GO</td>

   <td width="72">TB</td>

   <td width="96">7</td>

   <td width="102">09 00</td>

   <td width="144">3060 Derry Rd. E., Mississauga, ON</td>

   <td width="66">On time</td>

  </tr>

  <tr>

   <td width="78"><strong>31</strong></td>

   <td width="54">101</td>

   <td width="84">Union Station Bus Terminal</td>

   <td width="72">B</td>

   <td width="96">1</td>

   <td width="102">09 30</td>

   <td width="144">141 Bay Street, Toronto, ON</td>

   <td width="66">On time</td>

  </tr>

  <tr>

   <td width="78"><strong>31</strong></td>

   <td width="54">102</td>

   <td width="84">York Mills Bus Terminal</td>

   <td width="72">B</td>

   <td width="96">2</td>

   <td width="102">09 30</td>

   <td width="144">4023 Yonge St., North York, ON</td>

   <td width="66">On time</td>

  </tr>

  <tr>

   <td width="78"><strong>31</strong></td>

   <td width="54">103</td>

   <td width="84">Yorkdale Bus Terminal</td>

   <td width="72">B</td>

   <td width="96">3</td>

   <td width="102">09 30</td>

   <td width="144">1 Yorkdale Road, North York, ON</td>

   <td width="66">On time</td>

  </tr>

  <tr>

   <td width="78"><strong>31</strong></td>

   <td width="54">104</td>

   <td width="84">Bloor GO</td>

   <td width="72">T</td>

   <td width="96">4</td>

   <td width="102">09 30</td>

   <td width="144">1456 Bloor Street West, Toronto, ON</td>

   <td width="66">On time</td>

  </tr>

  <tr>

   <td width="78"><strong>31</strong></td>

   <td width="54">105</td>

   <td width="84">Weston GO</td>

   <td width="72">T</td>

   <td width="96">5</td>

   <td width="102">09 30</td>

   <td width="144">1865 Weston Road, Etobicoke, ON</td>

   <td width="66">On time</td>

  </tr>

  <tr>

   <td width="78"><strong>31</strong></td>

   <td width="54">106</td>

   <td width="84">Etobicoke North GO</td>

   <td width="72">TB</td>

   <td width="96">6</td>

   <td width="102">09 30</td>

   <td width="144">1949 Kipling Ave., Etobicoke, ON</td>

   <td width="66">On time</td>

  </tr>

  <tr>

   <td width="78"><strong>31</strong></td>

   <td width="54">107</td>

   <td width="84">Malton G O</td>

   <td width="72">TB</td>

   <td width="96">7</td>

   <td width="102">09 30</td>

   <td width="144">3060 Derry Rd. E., Mississauga, ON</td>

   <td width="66">On time</td>

  </tr>

  <tr>

   <td width="78"><strong>38A</strong></td>

   <td width="54">102</td>

   <td width="84">York Mills Bus Terminal</td>

   <td width="72">B</td>

   <td width="96">1</td>

   <td width="102">17 20</td>

   <td width="144">4023 Yonge St., North York, ON</td>

   <td width="66">Delayed</td>

  </tr>

  <tr>

   <td width="78"><strong>38A</strong></td>

   <td width="54">103</td>

   <td width="84">Yorkdale Bus Terminal</td>

   <td width="72">B</td>

   <td width="96">2</td>

   <td width="102">17 20</td>

   <td width="144">1 Yorkdale Road, North York, ON</td>

   <td width="66">Delayed</td>

  </tr>

  <tr>

   <td width="78"><strong>38A</strong></td>

   <td width="54">104</td>

   <td width="84">Bloor GO</td>

   <td width="72">T</td>

   <td width="96">3</td>

   <td width="102">17 20</td>

   <td width="144">1456 Bloor Street West, Toronto, ON</td>

   <td width="66">Delayed</td>

  </tr>

  <tr>

   <td width="78"><strong>38A</strong></td>

   <td width="54">105</td>

   <td width="84">Weston GO</td>

   <td width="72">T</td>

   <td width="96">4</td>

   <td width="102">17 20</td>

   <td width="144">1865 Weston Road, Etobicoke, ON</td>

   <td width="66">Delayed</td>

  </tr>

  <tr>

   <td width="78"><strong>38A</strong></td>

   <td width="54">106</td>

   <td width="84">Etobicoke North GO</td>

   <td width="72">TB</td>

   <td width="96">5</td>

   <td width="102">17 20</td>

   <td width="144">1949 Kipling Ave., Etobicoke, ON</td>

   <td width="66">Delayed</td>

  </tr>

 </tbody>

</table>

<strong>NOTE</strong>: TB corresponds to TRAIN AND BUS STATION

If time does not have a value in a row, it means the bus or the train does not stop at that stop.

<ol>

 <li>Given the above table structure, define the PK and justify your answer. Draw the dependency diagram. Label all transitive and/or partial dependencies. (<em>Hint</em>: This structure uses a composite primary key.)</li>

 <li>Remove all partial and transitive dependencies, draw the new dependency diagrams, and identify the normal forms for each table structure you created.</li>

 <li>Draw the Crow’s Foot ERD.</li>

 <li>We need to list all the stops per city. Alter the Stop table structure to allow such listing.</li>

</ol>




<strong> </strong>