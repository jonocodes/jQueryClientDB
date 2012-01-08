Instructions
------------

Include the clientdb plugin

      <script type="text/javascript" src="jquery-1.3.1.min.js"></script>
      <script type="text/javascript" src="jquery.clientdb.js"></script>

Put your XML data in a hidden div like so
 
      <div id="myDB" style="display: none;"><!--<xml>

        <bookstore>
          <book category="CHILDREN">
            <title>Harry Potter</title>
            <author>J K. Rowling</author>
            <year>2005</year>
            <price>29.99</price>
          </book>
          <book category="WEB">
            <title>XQuery Kick Start</title>
            <author>James McGovern</author>
            <year>2003</year>
            <price>49.99</price>
          </book>
        </bookstore>
       
      </xml>--></div>

Instantiate the database and query the JSON object.

      json = $.clientdb("#myDB");
      alert(json.bookstore.book[0].title); // displays "Harry Potter"

