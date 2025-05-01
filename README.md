<h1> XML Basics in SQL </h1>

<h2>Description</h2>
This project showcases how to extract and transform XML data using SQL Server. It begins by querying the `Person.Person` table for entries where the first name is 'John' and exporting the results as structured XML using `FOR XML PATH`, wrapping each entry in `<Person>` tags and enclosing the set within a `<Persons>` root. The resulting `XMLTest.xml` file is then imported using `OPENROWSET` and parsed with `sp_XML_preparedocument`. Using `OPENXML`, specific fields such as first name, middle name, and last name are extracted from each `<Person>` element and sorted by last name. This process demonstrates effective handling of hierarchical XML data in SQL Server for integration and data transformation tasks.

<br />

<h2>Languages and Utilities Used</h2>

- <b> SQL </b> 
- <b> XML </b>

<h2>Environments Used </h2>

- <b> Microsoft SQL Server </b>

<h2>Project walk-through:</h2>
<p align="left">
This SQL query selects all rows from the Person.Person table where the FirstName is 'John', <br/> and formats the result as XML using FOR XML PATH, wrapping each row in a <Person> tag <br/> and the entire output in a root <Persons> tag. <br/><br/>
  <img src="Screenshot 2025-04-17 202325.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
This XML output shows multiple <Person> elements, each representing a row where the first name <br/> is 'John' from the Person.Person table, including personal details and nested demographic <br/> data within the <Demographics> element, structured using SQL Server's FOR XML PATH feature <br/><br/>
  <img src="Screenshot 2025-04-17 202325.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
Confirmation of the successful creation of the XMLTest file. <br/><br/>
  <img src="Screenshot 2025-04-17 202325.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
This script reads an XML file into SQL Server, parses <Person> elements using OPENXML, and <br/> selects specific fields for each person, ordered by last name <br/><br/>
  <img src="Screenshot 2025-04-17 202325.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
 This script loads an XML file, extracts the <Person> elements using OPENXML, and retrieves <br/>only the first name, middle name, and last name of each person, sorted by last name.<br/><br/>
  <img src="Screenshot 2025-04-17 202325.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>


