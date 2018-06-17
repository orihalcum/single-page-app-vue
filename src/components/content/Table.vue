<template>

    <div id="table"></div>
    
</template>

<script>

    // import HotTable from 'vue-handsontable-official';
    import Handsontable from 'handsontable';
    import 'handsontable/dist/handsontable.full.css';
    import Vue from 'vue';
    
    export default {
        name: 'Table',
        data() {
            return {
                tableData: {}
            };
        },
        mounted(){
            this.fetchData();
        },
        methods: {
            fetchData(){
                let url = "https://services.bumntrack.com/api/news/list?limit=100";
                fetch(url)
                .then(res => res.json())
                .then(res => {
                    let arrayData = [];
                    res.value.forEach(element => {
                        arrayData.push([element.id, element.title, element.category.name, element.tags]);
                    });
                    console.log(arrayData);
                    var container = document.getElementById('table');
                    var hot = new Handsontable(container, {
                        data: arrayData,
                        colHeaders: ['ID', 'Title', 'Category', 'Tags']
                    })
                });
            }
        }
    }

</script>
