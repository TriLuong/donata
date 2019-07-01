<template>
    <div class="container-fluid event">
        <div class="row">
            <div class="col-md-3 left">  
                <h1>EVENTS</h1>
            </div>
            <div class="col-md-9 right">
                <img src="../assets/02-Lifestyle-photos/Donata_13Mar197750.jpg"/>
                <div class="container-fluid eventInfo">
                    <div class="row">
                        <div class="col-md-7 infoLeft">
                            <h1>DONATA ATVIFA 2019</h1>
                            <p>March 6-7th 2019</p>
                            <p>Secc 799 Nguyen Van Linh, Tan Phu, District 7, HCMC</p>
                        </div>
                        <div class="col-md-5 infoRight">
                            <div class="changePage">
                                <a href="#">&lt;</a>
                                <a href="#">&gt;</a>
                            </div>
                            <div class="eventDetail">
                                <a href="#">EVENT DETAILS &rarr;</a>
                            </div>
                            
                        </div>
                    </div>
                </div>
                
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "EventFirst",
}
</script>
<style lang="scss" scoped>
    .event{
        padding: 0 !important;
        .left{
            padding: 0;
            background-color: black;
            h1{
                color: gray;
                font-size: 150px;
                font-family: "Lato";
                font-weight: bold;
                transform: translateY(25rem) rotate(-90deg);
            }
        }
        .right{
            padding: 0;
            position: relative;
            img {
                width: 100%;
            }
            .eventInfo{
                position: absolute;
                bottom: 0;
                .infoLeft{
                    padding-left: 5rem;
                    text-align: left;
                    color: white;
                }
                .infoRight{
                    .changePage{
                        a{
                            text-decoration: none;
                            color: white;
                            font-size: 40px;
                            &:hover{
                                color:red;
                            }
                        }
                    }
                    .eventDetail{
                        color: white;
                        a{
                            position: absolute;
                            bottom: 1rem;
                            left: 0;
                            right: 0;
                            text-decoration: none;
                            font-family: "Lato";
                            color: white;
                            &:hover{
                                color:red;
                            }
                        }
                    }
                }
            }
        }
    }
    
</style>

