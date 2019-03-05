# vue-list-table

A simple, clean data table for VueJS (2.x) with essential features like sorting, column filtering, pagination etc

![Basic Screenshot](https://github.com/taegeum/vue-list-table/blob/master/images/crud-table.png)

## Live Demo

[vue-list-table Demo Site]()

## Getting Started

### Prerequisites

The plugin is meant to be used with existing Vue 2.x projects. It uses ES6 features so as long as your build process includes a transpiler, you're good to go.


### Installing

Install with github:
```
git clone https://github.com/taegeum/xxx.git 
```

import into project:
```
import Vue from 'vue';
import VueGoodTable from 'vue-good-table-sample';

Vue.use(VueGoodTable);
```

### Sample code
#### Example Usage 1

```html
<template>
  <div>
    <vue-good-table
      title="Demo Table"
      :columns="columns"
      :rows="rows"
      :paginate="true"
      :lineNumbers="true"/>
  </div>
</template>

<script>
export default {
  name: 'test',
  data(){
    return {
      columns: [
        {
          label: 'Name',
          field: 'name',
          filterable: true,
        },
        {
          label: 'Age',
          field: 'age',
          type: 'number',
          html: false,
          filterable: true,
        },
        {
          label: 'Created On',
          field: 'createdAt',
          type: 'date',
          inputFormat: 'YYYYMMDD',
          outputFormat: 'MMM Do YY',
        },
        {
          label: 'Percent',
          field: 'score',
          type: 'percentage',
          html: false,
        },
      ],
      rows: [
        {id:1, name:"John",age:20,createdAt: '201-10-31:9:35 am',score: 0.03343},
        {id:2, name:"Jane",age:24,createdAt: '2011-10-31',score: 0.03343},
        {id:3, name:"Susan",age:16,createdAt: '2011-10-30',score: 0.03343},
        {id:4, name:"Chris",age:55,createdAt: '2011-10-11',score: 0.03343},
        {id:5, name:"Dan",age:40,createdAt: '2011-10-21',score: 0.03343},
        {id:6, name:"John",age:20,createdAt: '2011-10-31',score: 0.03343},
        {id:7, name:"Jane",age:24,createdAt: '20111031'},
        {id:8, name:"Susan",age:16,createdAt: '2013-10-31',score: 0.03343},
        {id:9, name:"Chris",age:55,createdAt: '2012-10-31',score: 0.03343},
        {id:10, name:"Dan",age:40,createdAt: '2011-10-31',score: 0.03343},
        {id:11, name:"John",age:20,createdAt: '2011-10-31',score: 0.03343},
        {id:12, name:"Jane",age:24,createdAt: '2011-07-31',score: 0.03343},
        {id:13, name:"Susan",age:16,createdAt: '2017-02-28',score: 0.03343},
        {id:14, name:"Chris",age:55,createdAt: '',score: 0.03343},
        {id:15, name:"Dan",age:40,createdAt: '2011-10-31',score: 0.03343},
        {id:19, name:"Chris",age:55,createdAt: '2011-10-31',score: 0.03343},
        {id:20, name:"Dan",age:40,createdAt: '2011-10-31',score: 0.03343},
      ],
    };
  },
};
</script>
```


## Example Usage 2
<strong>Note:</strong> vue-good-table-sample also supports Search and CURD. 

```html
<vue-good-table 
    :columns="columns" 
    :rows="rows" 
    :paginate="true" 
    :globalSearch="true" 
    :sortable="false" 
    :onCreateClick="onCreateFn" 
    :onEditClick="onEditFn" 
    :onDeleteClick="onDeleteFn" 
    :externalSearchQuery="searchTerm" 
    styleClass="table table-striped"
/>

<script>
    export default {
        name: 'test',
        data() {
            return {
            columns: [{
                    label: 'Name',
                    field: 'name',
                    filterable: true,
                },
                {
                    label: 'Age',
                    field: 'age',
                    type: 'number',
                    html: false,
                    filterable: true,
                },
                {
                    label: 'Created On',
                    field: 'createdAt',
                    type: 'date',
                    inputFormat: 'YYYYMMDD',
                    outputFormat: 'MMM Do YY',
                },
                {
                    label: 'Percent',
                    field: 'score',
                    type: 'percentage',
                    html: false,
                },
            ],
            rows: [{
                    id: 1,
                    name: "John",
                    age: 20,
                    createdAt: '201-10-31:9:35 am',
                    score: 0.03343
                },
                {
                    id: 2,
                    name: "Jane",
                    age: 24,
                    createdAt: '2011-10-31',
                    score: 0.03343
                },
                {
                    id: 3,
                    name: "Susan",
                    age: 16,
                    createdAt: '2011-10-30',
                    score: 0.03343
                },
                {
                    id: 4,
                    name: "Chris",
                    age: 55,
                    createdAt: '2011-10-11',
                    score: 0.03343
                },
                {
                    id: 5,
                    name: "Dan",
                    age: 40,
                    createdAt: '2011-10-21',
                    score: 0.03343
                },
                {
                    id: 6,
                    name: "John",
                    age: 20,
                    createdAt: '2011-10-31',
                    score: 0.03343
                },
                {
                    id: 7,
                    name: "Jane",
                    age: 24,
                    createdAt: '20111031'
                },
                {
                    id: 8,
                    name: "Susan",
                    age: 16,
                    createdAt: '2013-10-31',
                    score: 0.03343
                },
                {
                    id: 9,
                    name: "Chris",
                    age: 55,
                    createdAt: '2012-10-31',
                    score: 0.03343
                },
                {
                    id: 10,
                    name: "Dan",
                    age: 40,
                    createdAt: '2011-10-31',
                    score: 0.03343
                },
                {
                    id: 11,
                    name: "John",
                    age: 20,
                    createdAt: '2011-10-31',
                    score: 0.03343
                },
                {
                    id: 12,
                    name: "Jane",
                    age: 24,
                    createdAt: '2011-07-31',
                    score: 0.03343
                },
                {
                    id: 13,
                    name: "Susan",
                    age: 16,
                    createdAt: '2017-02-28',
                    score: 0.03343
                },
                {
                    id: 14,
                    name: "Chris",
                    age: 55,
                    createdAt: '',
                    score: 0.03343
                },
                {
                    id: 15,
                    name: "Dan",
                    age: 40,
                    createdAt: '2011-10-31',
                    score: 0.03343
                },
                {
                    id: 19,
                    name: "Chris",
                    age: 55,
                    createdAt: '2011-10-31',
                    score: 0.03343
                },
                {
                    id: 20,
                    name: "Dan",
                    age: 40,
                    createdAt: '2011-10-31',
                    score: 0.03343
                }
            ]
            }
        },
        methods: {
            onCreateFn: function() {
                console.log("create fn");
            },
            onEditFn: function(row, index) {
                console.log("edit value:", row);
            },
            onDeleteFn: function(row, index) {
                console.log("delete value:", row);
            }
        }
    };
</script>
```
This should result in the screenshot seen above

### Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
