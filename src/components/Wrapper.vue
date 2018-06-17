<template>

    <div>
        <nav class="navbar navbar-custom navbar-fixed-top">
            <div class="container">
                <!-- Brand and toggle get grouped for better mobile display -->
                <div class="navbar-header">
                    <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1"
                        aria-expanded="false">
                        <span class="sr-only">Toggle navigation</span>
                        <span class="icon-bar"></span>
                        <span class="icon-bar"></span>
                        <span class="icon-bar"></span>
                    </button>
                    <!-- <a class="navbar-brand" href="index.html">
                        <img src="assets/images/brand-logo.png">
                    </a> -->
                    <button type="button" class="navbar-toggle-search collapsed hidden-lg hidden-md visible-sm visible-xs" data-toggle="collapse"
                        data-target="#bs-example-navbar-collapse-0" aria-expanded="false">
                        <span class="fa fa-search"></span>
                    </button>
                </div>

                <!-- Collect the nav links, forms, and other content for toggling -->
                <div class="row collapse" id="bs-example-navbar-collapse-0">
                    <div class="hidden-lg hidden-md visible-sm visible-xs">
                        <ul class="nav navbar-nav">
                            <li>
                                <form class="navbar-form">
                                    <div class="form-group">
                                        <input type="text" class="form-control" placeholder="Cari berita . . .">
                                        <!-- <i class="fa fa-search"></i> -->
                                    </div>
                                </form>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
                    <div class="visible-lg visible-md hidden-sm hidden-xs">
                        <ul class="nav navbar-nav navbar-right">
                            <li>
                                <a v-on:click="sidebarToggle">
                                    <span class="fa fa-cog"></span>
                                </a>
                            </li>
                            <li>
                                <a href="javascript:;">
                                    <span class="fa fa-question-circle"></span>
                                </a>
                            </li>
                            <li class="active">
                                <a href="javascript:;" class="nav-text">
                                    Dzulfan Fadli
                                </a>
                            </li>
                            <li>
                                <a href="index.html">
                                    <span class="fa fa-user"></span>
                                    <span class="sr-only">(current)</span>
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
                <!-- /.navbar-collapse -->

            </div>
            <!-- /.container-fluid -->
        </nav>
        <div class="main-content">

            <MainContent></MainContent>

            <!-- Sidebar Right -->
            <div class="sidebar sidebar-right " v-bind:class="{ active: isActive }">
                <div class="sidebar-title">
                    <span class="h3">Toolbox</span>
                    <span class="group-icons pull-right">
                    <a href="javascript:;" class="fa fa-refresh" v-on:click="refreshSidebar"></a>
                    <a href="javascript:;" class="fa fa-times" v-on:click="isActive = false"></a>
                    </span>
                </div>
                <div class="sidebar-body">
                    <ul class="list-unstyled">
                    <li>
                        <a href="javascript:;">
                        <span class="fa fa-search"></span> Search for a null
                        </a>
                    </li>
                    <li>
                        <a href="javascript:;">
                        <span class="fa fa-clone"></span> Copy records to another null
                        </a>
                    </li>
                    <li>
                        <a href="javascript:;">
                        <span class="fa fa-clipboard"></span> Hide Records
                        </a>
                    </li>
                    <li>
                        <a href="javascript:;">
                        <span class="fa fa-file"></span> Report Signature
                        </a>
                    </li>
                    <li>
                        <a href="javascript:;">
                        <span class="fa fa-file"></span> Problem Records
                        </a>
                    </li>
                    <li>
                        <a href="javascript:;">
                        <span class="fa fa-plug"></span> Apply Cable Connection Factor
                        </a>
                    </li>
                    <li>
                        <a href="javascript:;">
                        <label class="radio-inline">
                            <input type="radio" class="radio" name="radio-sidebar" v-model="form.radio.actualLength" value="">
                            <div class="radio-label">Actual Length</div>
                        </label>
                        </a>
                    </li>
                    <li>
                        <a href="javascript:;">
                        <label class="radio-inline">
                            <input type="radio" class="radio" name="radio-sidebar" v-model="form.radio.estimatedLength" value="">
                            <div class="radio-label">Estimated Length</div>
                        </label>
                        </a>
                    </li>
                    <li>
                        <div class="row m-t-10 m-b-10">
                        <div class="col-lg-6">
                            <button class="btn btn-md btn-define btn-default w-full">Define Unit</button>
                        </div>
                        <div class="col-lg-6">
                            <button class="btn btn-md btn-define btn-default w-full">Cable Type</button>
                        </div>
                        </div>
                        <div class="row m-b-20">
                        <div class="col-lg-6">
                            <input class="form-control w-full" v-model="form.define" placeholder="Define something">
                        </div>
                        <div class="col-lg-6">
                            <button class="btn btn-md btn-define btn-default w-full">Force DWG</button>
                        </div>
                        </div>
                    </li>
                    <li>
                        <a href="javascript:;">
                        <span class="fa fa-print"></span> Network Cable
                        </a>
                    </li>
                    <li>
                        <a href="javascript:;">
                        <span class="fa fa-print"></span> Weight
                        </a>
                    </li>
                    <li>
                        <a href="javascript:;">
                        <span class="fa fa-print"></span> Missing Equipment
                        </a>
                    </li>
                    <li>
                        <a href="javascript:;">
                        <span class="fa fa-print"></span> Cable Test Report
                        </a>
                    </li>
                    <li>
                        <a href="javascript:;">
                        <span class="fa fa-print"></span> Problems
                        </a>
                    </li>
                    <li>
                        <a href="javascript:;">
                        <span class="fa fa-file-excel-o"></span> Cable Schedule Export
                        </a>
                    </li>
                    </ul>
                </div>
                <div class="sidebar-footer">
                    <ul class="list-unstyled list-inline">
                    <li>
                        <a href="javascript:;" class="fa fa-desktop"></a>
                    </li>
                    <li>
                        <a href="javascript:;" class="fa fa-question-circle"></a>
                    </li>
                    </ul>
                </div>
            </div>

        </div>
    </div>

</template>

<script>

    import MainContent from "./MainContent.vue";

    export default {
        name: 'Wrapper',
        components: { MainContent },
        data() {
        return {
            isActive: false,
            form: {
                radio: {
                    actualLength : "",
                    estimatedLength : ""
                },
                define: ""
            }
        };
        },
        methods: {
        sidebarToggle: function(){
            this.isActive = !this.isActive;
        },
        refreshSidebar: function(){
                this.form = {
                    radio: {
                        actualLength : "",
                        estimatedLength : ""
                    },
                    define: ""
                }
        }
        }
    }

</script>

