<template>

    <div>

        <!--Nav Bar -->
        <nav class="navbar navbar-expand-lg navbar-light bg-light">
            
                <div class="collapse navbar-collapse" id="navbarTogglerDemo01" st>
                    <ul class="navbar-nav mr-auto mt-20 mt-lg-0" >
                    
                    <li class="nav-item" style="margin:15px;">
                        
                        <a class="nav-link" href="#">   
                        <!-- List Logo -->
                            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-list-ul" viewBox="0 0 16 16">
                                <path fill-rule="evenodd" d="M5 11.5a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9a.5.5 0 0 1-.5-.5zm-3 1a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm0 4a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm0 4a1 1 0 1 0 0-2 1 1 0 0 0 0 2z"/>
                            </svg>
                            SAVED LISTS 
                        </a>
                    </li>

                    <li class="nav-item" style="margin:15px;">
                        <a class="nav-link" href="#">         
                        <!-- Filter Logo -->
                            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-funnel" viewBox="0 0 16 16">
                                <path d="M1.5 1.5A.5.5 0 0 1 2 1h12a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-.128.334L10 8.692V13.5a.5.5 0 0 1-.342.474l-3 1A.5.5 0 0 1 6 14.5V8.692L1.628 3.834A.5.5 0 0 1 1.5 3.5v-2zm1 .5v1.308l4.372 4.858A.5.5 0 0 1 7 8.5v5.306l2-.666V8.5a.5.5 0 0 1 .128-.334L13.5 3.308V2h-11z"/>
                            </svg>
                            SAVED FILTERS
                        </a>
                    </li>

                    <li class="nav-item" style="margin:15px;">
                        <a class="nav-link" href="#">
                         <!-- Message Logo -->
                            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-arrow-clockwise" viewBox="0 0 16 16">
                                <path fill-rule="evenodd" d="M8 3a5 5 0 1 0 4.546 2.914.5.5 0 0 1 .908-.417A6 6 0 1 1 8 2v1z"/>
                                <path d="M8 4.466V.534a.25.25 0 0 1 .41-.192l2.36 1.966c.12.1.12.284 0 .384L8.41 4.658A.25.25 0 0 1 8 4.466z"/>
                            </svg>
                            SEARCH HISTORY
                        </a>
                    </li>
                    
                    </ul>


                    <form class="form-inline my-10 my-lg-0">
                        <input class="form-control mr-sm-3" type="text" name="" id="myInput" placeholder="Search.." v-on:keyup="searchFun()" width="300px">
                    </form>
                    
                    
                    
                </div>
        </nav>


        <!-- Table -->
        <div class="content-sidebar" >
            
            <div class="col">
                <div>
                   <div>
                    <table class="table" id="myTable">
                        <thead>
                            <tr>
                                <th scope="col">Date</th>
                                <th scope="col">Name</th>
                                <th scope="col">Age</th>
                                <th scope="col">Action</th>
                                <th scope="col">Programming Skills</th>
                            </tr>
                        </thead>
                        <tbody>
                        <tr v-for="data in list" :key="data.id">
                                <td>{{data.Date}}</td>
                                <td>{{data.name}}</td>
                                <td>{{data.age}}</td>

                                <td>
                                    <!-- Icon -->
                                     <!-- Message Logo -->
                                    <a href="#" style="margin:10px;">
                                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-envelope" viewBox="0 0 16 16">
                                            <path d="M0 4a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V4zm2-1a1 1 0 0 0-1 1v.217l7 4.2 7-4.2V4a1 1 0 0 0-1-1H2zm13 2.383-4.758 2.855L15 11.114v-5.73zm-.034 6.878L9.271 8.82 8 9.583 6.728 8.82l-5.694 3.44A1 1 0 0 0 2 13h12a1 1 0 0 0 .966-.739zM1 11.114l4.758-2.876L1 5.383v5.73z"/>
                                        </svg>
                                    </a>

                                     <!-- Share Logo -->
                                    <a href="#" style="margin:10px;">
                                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-share" viewBox="0 0 16 16">
                                            <path d="M13.5 1a1.5 1.5 0 1 0 0 3 1.5 1.5 0 0 0 0-3zM11 2.5a2.5 2.5 0 1 1 .603 1.628l-6.718 3.12a2.499 2.499 0 0 1 0 1.504l6.718 3.12a2.5 2.5 0 1 1-.488.876l-6.718-3.12a2.5 2.5 0 1 1 0-3.256l6.718-3.12A2.5 2.5 0 0 1 11 2.5zm-8.5 4a1.5 1.5 0 1 0 0 3 1.5 1.5 0 0 0 0-3zm11 5.5a1.5 1.5 0 1 0 0 3 1.5 1.5 0 0 0 0-3z"/>
                                        </svg>
                                    </a>

                                     <!-- edit Logo -->
                                    <a href="#" style="margin:10px;">

                                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-pencil" viewBox="0 0 16 16">
                                            <path d="M12.146.146a.5.5 0 0 1 .708 0l3 3a.5.5 0 0 1 0 .708l-10 10a.5.5 0 0 1-.168.11l-5 2a.5.5 0 0 1-.65-.65l2-5a.5.5 0 0 1 .11-.168l10-10zM11.207 2.5 13.5 4.793 14.793 3.5 12.5 1.207 11.207 2.5zm1.586 3L10.5 3.207 4 9.707V10h.5a.5.5 0 0 1 .5.5v.5h.5a.5.5 0 0 1 .5.5v.5h.293l6.5-6.5zm-9.761 5.175-.106.106-1.528 3.821 3.821-1.528.106-.106A.5.5 0 0 1 5 12.5V12h-.5a.5.5 0 0 1-.5-.5V11h-.5a.5.5 0 0 1-.468-.325z"/>
                                        </svg>
                                    </a>

                                     <!-- delete Logo -->
                                    <a href="#" style="margin:10px;">
                                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-trash" viewBox="0 0 16 16">
                                            <path d="M5.5 5.5A.5.5 0 0 1 6 6v6a.5.5 0 0 1-1 0V6a.5.5 0 0 1 .5-.5zm2.5 0a.5.5 0 0 1 .5.5v6a.5.5 0 0 1-1 0V6a.5.5 0 0 1 .5-.5zm3 .5a.5.5 0 0 0-1 0v6a.5.5 0 0 0 1 0V6z"/>
                                            <path fill-rule="evenodd" d="M14.5 3a1 1 0 0 1-1 1H13v9a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V4h-.5a1 1 0 0 1-1-1V2a1 1 0 0 1 1-1H6a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1h3.5a1 1 0 0 1 1 1v1zM4.118 4 4 4.059V13a1 1 0 0 0 1 1h6a1 1 0 0 0 1-1V4.059L11.882 4H4.118zM2.5 3V2h11v1h-11z"/>
                                        </svg>
                                    </a>
                                </td>

                                <td><button type="button" @click="showDetails(data.programming)" class="btn btn-light">Details</button></td>
                            </tr>
                        </tbody>
                    </table>
                   </div>
                </div>
            </div>


            <!-- Details -->
            <div class="col">
                <h3>Skills Description</h3>
                <table class="table">
                    <tr v-for="skill in sks" :key="skill.id">
                        <td>{{skill}}</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>
</template>





<script>

    import json from 'D:/VeuJs/Task1/app/src/assets/Datafile.json'                  //** path for json flie

    export default {
        name:'Index1',

        data(){
            return{
                list:json.employees,
                sks:[],
                filter:"",
                myTab:"",
                tr:"",
                td:"",
                textvalue:"",

            }
        },

        methods:{
            showDetails(id)
            {
                //alert(id);
                this.sks=id;
            },

            searchFun(){
            
                this.filter =document.getElementById('myInput').value.toUpperCase();
                this.myTab =document.getElementById('myTable');
                this.tr=this.myTab.getElementsByTagName('tr');

                for(var i=0; i<this.tr.length;i++)
                {
                    this.td= this.tr[i].getElementsByTagName('td')[1];

                    if(this.td)
                    {
                        this.textvalue = this.td.textContent || this.td.innerHTML;

                        if(this.textvalue.toUpperCase().indexOf(this.filter) == -1)
                        {
                            this.tr[i].style.display = "none";
                        }
                        else
                        {
                            this.tr[i].style.display="";
                        }
                    }
                }
            },

        },

        components: {
        // Data
        }


    }

</script>



<style scoped>

        .content-sidebar{
            display: flex;
            flex-wrap: wrap;
        }

        .content-sidebar > *:nth-child(1)
        {
            flex: 1 1 70%;
            
            border-style: outset;
        }

        .content-sidebar > *:nth-child(2)
        {
            flex: 1 1 30%;
        }

</style>