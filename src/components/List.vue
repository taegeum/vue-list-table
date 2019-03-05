<template>
  <div class="list">
    <input type="text" id="search" class="form-control" v-model="searchTerm" placeholder="검색 ">
    <br>
    <vue-good-table :columns="columns" :rows="rows" :paginate="true" :globalSearch="true" :sortable="false" :onCreateClick="onCreateFn" :onEditClick="onEditFn" :onDeleteClick="onDeleteFn" :externalSearchQuery="searchTerm" styleClass="table table-striped"
    />
  </div>
</template>

<script>
  export default {
    name: "List",
    data() {
      return {
        msg: "Welcome to Your Vue.js App",
        searchTerm: "",
        columns: [{
            label: "Name",
            field: "name",
            filterable: true
          },
          {
            label: "Age",
            field: "age",
            type: "number",
            html: false,
            filterable: true
          },
          {
            label: "Created On",
            field: "createdAt",
            type: "date",
            inputFormat: "YYYYMMDD",
            outputFormat: "MMM Do YY"
          },
          {
            label: "Percent",
            field: "score",
            type: "percentage",
            html: false
          }
        ],
        rows: [{
            id: 1,
            name: "John",
            age: 20,
            createdAt: "201-10-31:9:35 am",
            score: 0.03343
          },
          {
            id: 2,
            name: "Jane",
            age: 24,
            createdAt: "2011-10-31",
            score: 0.03343
          },
          {
            id: 3,
            name: "Susan",
            age: 16,
            createdAt: "2011-10-30",
            score: 0.03343
          },
          {
            id: 4,
            name: "Chris",
            age: 55,
            createdAt: "2011-10-11",
            score: 0.03343
          },
          {
            id: 5,
            name: "Dan",
            age: 40,
            createdAt: "2011-10-21",
            score: 0.03343
          },
          {
            id: 6,
            name: "John",
            age: 20,
            createdAt: "2011-10-31",
            score: 0.03343
          },
          {
            id: 7,
            name: "Jane",
            age: 24,
            createdAt: "20111031"
          },
          {
            id: 8,
            name: "Susan",
            age: 16,
            createdAt: "2013-10-31",
            score: 0.03343
          },
          {
            id: 9,
            name: "Chris",
            age: 55,
            createdAt: "2012-10-31",
            score: 0.03343
          },
          {
            id: 10,
            name: "Dan",
            age: 40,
            createdAt: "2011-10-31",
            score: 0.03343
          },
          {
            id: 11,
            name: "John",
            age: 20,
            createdAt: "2011-10-31",
            score: 0.03343
          },
          {
            id: 12,
            name: "Jane",
            age: 24,
            createdAt: "2011-07-31",
            score: 0.03343
          },
          {
            id: 13,
            name: "Susan",
            age: 16,
            createdAt: "2017-02-28",
            score: 0.03343
          },
          {
            id: 14,
            name: "Chris",
            age: 55,
            createdAt: "",
            score: 0.03343
          },
          {
            id: 15,
            name: "Dan",
            age: 40,
            createdAt: "2011-10-31",
            score: 0.03343
          },
          {
            id: 19,
            name: "Chris",
            age: 55,
            createdAt: "2011-10-31",
            score: 0.03343
          },
          {
            id: 20,
            name: "Dan",
            age: 40,
            createdAt: "2011-10-31",
            score: 0.03343
          }
        ]
      };
    },
    methods: {
      onCreateFn: function() {
        alert("create fn");
        console.log("create fn");
      },
      onEditFn: function(row, index) {
        alert("edit fn", row);
        console.log("edit value:", row);
      },
      onDeleteFn: function(row, index) {
        alert("delete fn", row);
        console.log("delete value:", row);
      }
    }
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1,
  h2 {
    font-weight: normal;
  }
  
  ul {
    list-style-type: none;
    padding: 0;
  }
  
  li {
    display: inline-block;
    margin: 0 10px;
  }
  
  a {
    color: #42b983;
  }
</style>
