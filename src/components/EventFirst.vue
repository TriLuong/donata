<template>
    <div class="container-fluid event">
        <div class="row">
            <div class="col-md-3 left">  
                <h1>EVENTS</h1>
            </div>
            <div class="col-md-9 right">
                <img v-bind:src="require('../assets/02-Lifestyle-photos/' + this.items[count].url)"/>
                <div class="container-fluid eventInfo">
                    <div class="row">
                        <div class="blurColor" />
                        <div class="col-md-7 infoLeft">
                            <h1>DONATA ATVIFA 2019</h1>
                            <p><i class="fas fa-calendar-alt"></i> March 6-7th 2019</p>
                            <p><i class="fas fa-map-marker-alt"></i> Secc 799 Nguyen Van Linh, Tan Phu, District 7, HCMC</p>
                        </div>
                        <div class="col-md-5 infoRight">
                            <div class="changePage">
                                <a class="previous" v-on:click="nextContent(-1)">&lt;</a>
                                <a class="next" v-on:click="nextContent(1)">&gt;</a>
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
        data() {
        return {
            count: 0,
            items: [
                {
                    id: 1,
                    url: "Donata_13Mar197750.jpg",
                },
                {
                    id: 2,
                    url: "Donata_13Mar197740.jpg",
                },
                {
                    id: 3,
                    url: "Donata_13Mar197798.jpg",
                },
            ],
        }
    },
    methods: {
        nextContent: function(indeX) {
            this.count += indeX;
 
            if(this.count > this.items.length - 1){
                this.count = 0;
            }
            else if (this.count < 0) {
                this.count = this.items.length - 1;
            }
        }
    }
}
</script>
<style lang="scss" scoped>
    .event{
        padding:0;
        .left{
            padding: 0;
            background-color: black;
            h1{
                color: gray;
                font-size: 100px;
                font-family: "Lato";
                font-weight: bold;
                transform: translateY(280px) rotate(-90deg);
            }
        }
        .right{
            padding: 0;
            position: relative;
            img {
                width: 100%;
                object-fit: cover;
                height: 100vh;
                min-height: 600px;
            }
            .eventInfo{
                position: absolute;
                bottom: 0;
                .blurColor {
                    position: absolute;
                    bottom: 0;
                    left: 0;
                    right: 0;
                    background-image: linear-gradient(transparent, black);
                    height: 70vh;
                    min-height: 300px;
                }
                .infoLeft{
                    padding: 0;
                    text-align: left;
                    color: white;
                    i {
                        padding-right: 10px;
                    }
                }
                .infoRight{
                    .changePage{
                        a{
                            text-decoration: none;
                            color: white;
                            font-size: 40px;
                            display: inline-block;
                            padding: 0 10px;
                            line-height: 40px;
                            cursor: pointer;
                            &:hover{
                                background-color: gainsboro;
                                color: black;
                                opacity: 0.6;
                                border-radius: 10px;
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
                            font-weight: bold;
                            width: 70%;
                            padding: 10px;
                            margin: auto;
                            &:hover{
                                background-color: gainsboro;
                                color: black;
                                border-radius: 10px;
                            }
                        }
                    }
                }
            }
        }
    }
    
    @media screen and (max-width: 736px) {
        .event{
            background-color: black;
            padding:  1rem 2rem 2rem !important;
            height: 100vh;
            min-height: 350px;
            overflow: hidden;
            .left{
                h1{
                    transform: none;
                    font-size: 65px;
                }
            }
            .right{
                img {
                    object-fit: cover;
                    height: 270px;
                    min-height: 250px;
                }
                 .eventInfo{
                    top: 1rem;
                    padding: 0;
                    margin: 0;
                    .infoLeft{
                        padding-left: 1rem;
                    }
                    .infoRight{
                        padding: 0;
                        .changePage{
                            position: absolute;
                            top: 40px;
                            left:0;
                            right: 0;
                            a{
                                display: inline-block;
                                padding:10px 55px;
                                background-color: gray;
                                border: 1px solid gray;
                                border-radius: 10px;
                                margin: 5px;
                                &:hover {
                                    color: white;
                                    background-color: rgb(85, 84, 84);
                                    opacity: 1;
                                }
                            }
                        }
                        .eventDetail{
                            text-align: left;
                            padding-left: 1rem;
                            a{
                                position: static;
                            }
                            
                        }
                    }
                 }
            }
        }
        @media screen and (max-width: 414px) {
            .event{
                .left{
                    h1{
                        font-size: 72px;
                    }
                }
                .right{
                    img {
                        height: 495px;
                    }
                    .eventInfo{
                        top: 8rem;
                    }
                }
            }
        }
    }
</style>

