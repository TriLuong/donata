<template>
    <div class="container-fluid publication">
        <div class="row">
            <div class="col-md-6 col-sm-6 publicLeft">
                <p>Collection</p>
                <h1>LATEST PUBLICATIONS</h1>
                <p>Sed vulputate lorem ut bibendum elementum. Phasellus placerat elit arcu, at imperdiet augue ullamcorper id. Maecenas malesuada leo libero. </p>
                <a href="#">VIEW ALL ARTICLES &rarr;</a>
            </div>
            <div class="col-md-6 col-sm-6 publicRight">
                <div class="container-fluid">
                    <div class="row">
                        <div class="col-md-8 col-sm-6 publicRightContent">
                            <img v-bind:src="require('../assets/02-Lifestyle-photos/' + this.items[count].url)"/>
                            <div class="blurColor" />
                            <div class="publicRightTitle">
                                <p>{{this.items[count].content}}</p>
                                <p>{{this.items[count].time}}</p>
                            </div>
                        </div>
                        <div class="col-md-4 col-sm-6 publicRightCarousel">
                            <img v-bind:src="require('../assets/02-Lifestyle-photos/' + this.items[nextCount].url)"/>
                            <div class="changePage">
                                <a class="previous" v-on:click="nextContent(-1)">&lt;</a>
                                <a class="next" v-on:click="nextContent(1)">&gt;</a>
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
    name: "Public",
    data() {
        return {
            count: 0,
            nextCount:1,
            items: [
                {
                    id: 1,
                    url: "Donata_13Mar197829.jpg",
                    content: "Cras ullamcorper gravida mi sit amet pellen tesque. Sed non purus nullan teger commodo ac.",
                    time: "June 20th 2019",
                },
                {
                    id: 2,
                    url: "Donata_13Mar197766.jpg",
                    content: "Cras ullamcorper gravida mi sit amet pellen tesque. Sed non purus nullanteger commodo ac.",
                    time: "July 20th 2019",
                },
                {
                    id: 3,
                    url: "Donata_13Mar197789.jpg",
                    content: "Cras ullamcorper gravida mi sit amet pellen tesque.",
                    time: "September 20th 2019",
                },
            ],
        }
    },
    methods: {
        nextContent: function(indeX) {
            this.count += indeX;
            this.nextCount += indeX;
 
            if(this.count > this.items.length - 1){
                this.count = 0;
            }
            else if (this.count < 0) {
                this.count = this.items.length - 1;
            }
            if(this.nextCount > this.items.length - 1){
                this.nextCount = 0;
            }
            else if(this.nextCount < 0) {
                this.nextCount = this.items.length - 1;
            } 
        }
    }
}
</script>

<style lang="scss" scoped>
    .publication{
        padding: 5rem 0 5rem 5rem;
        height: 100vh;
        min-height: 600px;
        .publicLeft {
            padding-right: 5rem;
            text-align: left;
            position: relative;
            p:first-child {
                text-transform: uppercase;
                font-weight: bold;
            }
            h1 {
                text-transform: uppercase;
                font-weight: bold;
            }
            a {
                position: absolute;
                text-decoration: none;
                color: black;
                font-weight: bold;
                bottom: 0;
                padding: 10px;
                &:hover {
                    background-color: gray;
                    color: white;
                    border-radius: 10px;
                }
            }
        }
        .publicRight {
            padding:0;
            padding-left: 2rem;
            & > div {
                padding: 0;
            }
            img {
                width: 100%;
                height: 100vh;
                max-height: 450px;
                min-height: 400px;
            }
            .publicRightContent{
                padding:0;
                img {
                    position: relative;
                    width: 100%;
                }
                .blurColor {
                    position: absolute;
                    bottom: 0;
                    left: 0;
                    right: 0;
                    background-image: linear-gradient(transparent, black);
                    height: 50vh;
                    min-height: 300px;
                }
                .publicRightTitle{
                    position: absolute;
                    bottom: 0;
                    padding: 2rem;
                }
                p {
                    font-weight: bold;
                    color:white;
                    text-align: left;
                }
                p:last-child {
                    text-transform: uppercase;
                    color: gray;
                }
            }
            .publicRightCarousel {
                color: white;
                padding: 0;
                padding-left: 10px;
                position: relative;
                img{
                    position: relative;
                    object-fit: cover;
                }   
                
                & > .changePage {
                    & > a.previous {
                        display: none;
                    }
                    & > a {
                        cursor: pointer;
                        font-size: 50px;
                        text-decoration: none;
                        color: white;
                        position: absolute;
                        top:0;
                        bottom:0;
                        left:10px;
                        right:0;
                        padding-top: 10rem;
                        background-color: black;
                        opacity: 0.5;
                        &:hover {
                            opacity: 0.7;
                        }
                    }
                }
            }
        }
    }
    @media screen and (max-width: 1366px) {
        .publication {
            .publicRight {
                .publicRightContent{
                    .blurColor {
                        height: 30vh;
                    }
                }
            }
        }
    }

    @media screen and (max-width: 736px) {
        .publication {
            padding: 2rem;
            padding-right: 0;
            height: 100vh;
            min-height: 350px;
            .publicLeft {
                height: 85vh;
            }
            .publicRight {
                height: 85vh;
                overflow: hidden;
                .publicRightContent{
                    .blurColor {
                        height: 95vh;
                    }
                    .publicRightTitle{
                        top: 2rem;
                    }
                }
                .publicRightCarousel {
                     & > .changePage {
                        & > a {
                            padding-top:9rem;
                        }
                     }
                }
            }
        }
    }

    @media screen and (max-width: 414px) {
        .publication {
            padding: 2rem;
            height: 100vh;
            min-height: 350px;
            .publicLeft {
                padding: 0;
                height: auto;
                p{
                    font-size: 14px;
                }
                a {
                    position: static;
                }
            }
            .publicRight {
                padding: 0;
                margin-top: 1rem ;
                img {
                    width: 100%;
                    position: static;
                    object-fit: cover;
                    max-height: 230px;
                    min-height: 230px;
                }
                .publicRightContent{
                    padding: 0;
                    .blurColor {
                        height: 30vh;
                        min-height: 200px;
                    }
                }
                .publicRightCarousel {
                    margin-top: 10px;
                    padding:0;
                    & > img{
                        display: none;
                        position: static;
                    }
                    & > .changePage {
                        position: static;
                        & > a {
                            position: static;
                            display: inline-block !important;
                            padding: 1px 60px;
                            border: 1px solid gray;
                            background-color: gray;
                            border-radius: 5px;
                            transform: translateY(0);
                        }
                        & > a:first-child {
                            margin-right: 4px;
                        }
                        & > a:last-child {
                            margin-left: 4px;
                        }
                        & > a:hover {
                            border-radius: 5px;
                            color: black;
                        }
                    }
                }
            }
        }
    }
</style>

