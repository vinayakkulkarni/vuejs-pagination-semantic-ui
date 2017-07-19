# Vue Pagination for Semantic-UI :zap:
+ This is [on GitHub](https://github.com/vinayakkulkarni/vuejs-pagination-semantic-ui) so let me know if I've messed it somewhere, give me a star :star: if you like it, :beers:
+ Server-side paging component in vue, template based on Semantic-UI.

* [Vue.js](https://vuejs.org/) (2.x)
* [Semantic-UI CSS](https://semantic-ui.com/) (2.x.x)

### :white_check_mark: Installation :ok_hand:

```bash
$ npm install vuejs-pagination-semantic-ui
```

### :white_check_mark: Usage :mortar_board:
```js
import pagination from 'vuejs-pagination-semantic-ui'
    
new Vue({
  el: '#app',,
  components: { pagination }
  data () {
    return {
      total: 1000,
      pageSize: 50,
      paginationOptions: { // Not required to pass this configurations
		    offset: 2,
        previousText: 'Prev',
        nextText: 'Next',
        alwaysShowPrevNext: true
      }
    }
  },
  methods: {
    pageChanged (page) {            
      console.log(page)
      // Exec your response to server passing 'page' params as clicked button paging
    }
  }
})
```

### :white_check_mark: Example :four_leaf_clover: 

```html
<body id="app">
  <pagination :total="total" :page-size="pageSize" :callback="pageChanged" :options="paginationOptions">
  </pagination>
</body>
```

### :white_check_mark: :book: Props: 
| Name          | Type     | Default | Required | Description
| :------------ | :--------| :-------| :--------| :-----------
| total         | Number   |         | true     | Total items in server side
| pageSize      | Number   |         | true     | Number of items in page
| callback      | Function |         | true     | Callback function used to load data for selected page

### :white_check_mark: :book: Options: 
| Name                | String  | Default     | Description
| :-------------------| :-------| :-----------| :-------
| offset              | Number  | 3           | Left and right offset of pagination numbers to display
| previousText        | String  | «           | Change default previous button text
| nextText            | String  | »           | Change default next button text
| alwaysShowPrevNext  | Boolean | false       | Show prev/next button even if on first/last page

## NPM :octocat:  

[![NPM](https://nodei.co/npm/vuejs-pagination-semantic-ui.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/vuejs-pagination-semantic-ui/)

## License :book:
+ MIT
