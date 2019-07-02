<template>
    <div class="container-fluid publication">
        <div class="row">
            <div class="col-md-6 publicLeft">
                <p>Collection</p>
                <h1>LATEST PUBLICATIONS</h1>
                <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
                <a href="#">VIEW ALL ARTICLES &rarr;</a>
            </div>
            <div class="col-md-6 publicRight">
                <div class="row">
                    <div class="col-md-8 publicRightContent">
                        <img v-bind:src="require('../assets/02-Lifestyle-photos/' + this.items[count].url)"/>
                        <div class="publicRightTitle">
                            <p>{{this.items[count].content}}</p>
                            <p>{{this.items[count].time}}</p>
                        </div>
                    </div>
                    <div class="col-md-4 publicRightCarousel">
                        <img v-bind:src="require('../assets/02-Lifestyle-photos/' + this.items[nextCount].url)"/>
                        <div class="changePage">
                            <a v-on:click="nextContent">&gt;</a>
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
                    content: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
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
                    content: "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
                    time: "September 20th 2019",
                },
            ],
        }
    },
    methods: {
        nextContent: function() {
            this.count +=1;
            this.nextCount += 1;
            console.log("Publication count",this.count);
            if(this.count > this.items.length - 1){
                this.count = 0;
            }
            if(this.nextCount > this.items.length - 1){
                this.nextCount = 0;
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
        overflow-y: hidden;
        .publicLeft {
            padding-right: 15rem;
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
                &:hover {
                    color: red;
                }
            }
        }
        .publicRight {
            padding-left: 2rem;
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
                }
            }
            .publicRightCarousel {
                color: white;
                img{
                    position: relative;
                }   
                
                .changePage {
                    position: absolute;
                    top:0;
                    bottom:0;
                    left:0;
                    right: 0;
                    a {
                        font-size: 50px;
                        text-decoration: none;
                        cursor: pointer;
                        color: blue;
                        &:hover {
                            color: red;
                        }
                    }
                }
            }
        }
    }
</style>

