# ilookup

Example Code:

```
$('.student_lookup').iLookup({
  url: "http://mikooldemo.akonto.ltd/admin/student_search",
  id: 'id',
  display: 'first_name',
  search_btn: '<span class="glyphicon glyphicon-search" aria-hidden="true"></span>',
  one_field_search: false,
  columns: [
    {col_name: 'id', col_alias: 'Reg. No.', is_searchable: true, modifier: null},
    {col_name: 'first_name', col_alias: 'First Name', is_searchable: true, modifier: null},
    {col_name: 'last_name', col_alias: 'Last Name', is_searchable: true, modifier: null},
    {col_name: 'picture', col_alias: 'Picture', is_searchable: false, modifier: function(item){
      if(item)
          item = '<img style="width:100%; max-width: 200px;" src="'+asset_path+item+'">';
        else
          item = '';

      return item;
    }},
    {col_name: 'section_name', col_alias: 'Section', is_searchable: true, modifier: null},
    {col_name: 'grade_name', col_alias: 'Grade', is_searchable: true, modifier: null},
    {col_name: 'branch_name', col_alias: 'Branch', is_searchable: true, modifier: null},
  ],
  on_select: function(obj){

  },
});
```
