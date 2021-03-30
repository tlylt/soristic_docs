<variable name="example">
To inject this HTML segment in your markbind files, use {{ example }} where you want to place it.
More generally, surround the segment's id with double curly braces.
</variable>

<variable name="guide">
<div id="guide-table"></div>
<script>
      var tabledata = fetch("url")
        .then((response) => response.json())
        .then((data) => {
          //create Tabulator on DOM element with id "example-table"
          var table = new Tabulator("#guide-table", {
            data: data, //assign data to table
            layout: "fitDataStretch", //fit columns to width of table (optional)
            responsiveLayout:"collapse",
            columns: [
              //Define Table Columns
              {title: "Date", field: "date"},
              {title: "Time", field: "time"},
              { title: "Name", field: "name"},
              {
                title: "Email",
                field: "email",
                hozAlign: "left",
              },
              {
                title: "Organisation",
                field: "organisation",
              },
              {
                title: "Publication",
                field: "publication",
              },
            ],
          });
        });
    </script>
</variable>

<variable name="game">
<div id="game-table"></div>
<script>
      var tabledata = fetch("url")
        .then((response) => response.json())
        .then((data) => {
          //create Tabulator on DOM element with id "example-table"
          var table = new Tabulator("#game-table", {
            data: data, //assign data to table
            layout: "fitColumns", //fit columns to width of table (optional)
            responsiveLayout:"collapse",
            columns: [
              {title: "Date", field: "date"},
              {title: "Time", field: "time"},
              { title: "Age", field: "age"},
              {
                title: "Gender",
                field: "gender",
                hozAlign: "left",
              },
              {
                title: "Game",
                field: "game",
              }
            ],
          });
        });
</script>
</variable>
<variable name="feedback">
<div id="game-feedback-table"></div>
<script>
      var tabledata = fetch("url")
        .then((response) => response.json())
        .then((data) => {
          //create Tabulator on DOM element with id "example-table"
          var table = new Tabulator("#game-feedback-table", {
            data: data, //assign data to table
            layout: "fitColumns", //fit columns to width of table (optional)
            responsiveLayout:"collapse",
            columns: [
              {title: "Date", field: "date"},
              {title: "Time", field: "time"},
              { title: "Enjoyable", field: "enjoyable"},
              {
                title: "Difficult",
                field: "difficult",
                hozAlign: "left",
              },
              {
                title: "Favourite Character",
                field: "favourite",
              },
              {
                title: "Least Favourite Character",
                field: "least_favourite",
              },
              {
                title: "Game",
                field: "game",
              }
            ],
          });
        });
</script>
</variable>
<variable from="variables.json" />
