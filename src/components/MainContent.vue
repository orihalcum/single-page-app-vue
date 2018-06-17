<template>

    <div id="content-body" class="content-body">

        <div class="content-title">
            <div class="col-lg-12" style="text-align: center">
                <span class="h2 counter">
                    <i class="fa fa-calendar"></i>
                    100
                </span>
                <span class="h1 title">Cable Schedule</span>
                <div class="pagination">
                    <a href="#1">1</a>
                    <a href="#2">2</a>
                    <a href="#3">3</a>
                    <a href="#4">4</a>
                </div>
            </div>
        </div>

        <div class="content-table">
            <Table></Table>
        </div>

    </div>

</template>

<script>

    import Table from './content/Table.vue';

    export default {
        name: 'MainContent',
        components: { Table },
        data() {
            return {};
        },
        methods: {}
    }

</script>

