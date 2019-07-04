<template>
    <footer class="container-fluid">
        <div class="row footerTop">
            <div class="col-md-6">
                <h1>#DONATALIFESTYLE</h1>
            </div>
            <div class="col-md-6">
                <p>Sed vulputate lorem ut bibendum elementum. Phasellus placerat elit arcu, at imperdiet augue ullamcorper id. Maecenas malesuada leo libero. </p>
            </div>
           
            <div class="footerImg">
                <div class="col-md-4">
                    <img v-bind:src="require('../assets/02-Lifestyle-photos/' + this.items[count].url)"/>
                </div>
            </div>

            <div class="changePage">
                <a class="previous" v-on:click="nextContent(-1)">&lt;</a>
                <a class="next" v-on:click="nextContent(1)">&gt;</a>
            </div>
        </div>

        

        <div class="row footerBottom">
            <div class="row footerBottomContact">
                <div class="col-md-4 logo">
                    <a href="#"><img src="../assets/logo.svg"/></a>
                </div>
                <div class="col-md-8 info">
                    <div class="row">
                        <ul class="col-md-4">
                            <h6>Contact</h6>
                            <li>+84 937 991 235</li>
                            <li>malene@donata-inc.com</li>
                            <li>www.donata-inc.com</li>
                        </ul>
                        <ul class="col-md-4">
                            <h6>Address</h6>
                            <li>198C1 Nguyen Van Huong, Thao Dien, District 2, Ho Chi Minh City</li>
                        </ul>
                        <ul class="col-md-4">
                            <h6>working time</h6>
                            <li>Monday to Friday
                            (9AM to 5PM). By appointment only.</li>
                            <li>Please call our office to make an appointment</li>

                        </ul>
                    </div>
                </div>
            </div>

            <div class="container-fluid">
                <div class="row footerBottomCopyright">
                    <div class="col-md-6 left">
                        <p>&copy; 2019 Donata Inc.</p>
                    </div>
                    <div class="col-md-6 right">
                        <p>Website by <img src="../assets/conceptual.svg"/></p>
                    </div>
                </div>
            </div>
        </div>
        
        
        
    </footer>
</template>

<script async>
export default {
    name:"Footer",
    data() {
        return {
            count: 0,
            items: [
                {
                    id: 1,
                    url: "Donata_13Mar197775.jpg",
                },
                {
                    id: 2,
                    url: "Donata_13Mar197838.jpg",
                },
                {
                    id: 3,
                    url: "Donata_13Mar197791.jpg",
                },
            ],
        }
    },
    methods: {
        nextContent: function(indeX) {
            console.log(typeof(indeX));
            this.count += parseInt(indeX);
 
            console.log("Publication count", this.count);
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
    footer {
        padding: 0;
        height: 100vh;
        min-height: 600px;
        .footerTop {
            position: relative;
            background-color: black;
            color: white;
            padding: 3rem 3rem;
            height: 300px;
            h1 {
                text-transform: uppercase;
            }
            p{
                text-align: left;
            }
            p:last-child{
                padding-left: 30px;
            }
            .footerImg{
                position: absolute;
                top: 190px;
                img {
                    object-fit: cover;
                    width:250px;
                    height:250px;
                }
                div:first-child {
                    text-align: left;
                }
                div:last-child {
                    text-align: right;
                }
            }
            .changePage{
                display: none;
            }
        }
        
        .footerBottom {
            margin: 0 30px !important;
            .footerBottomContact{
                padding-bottom: 5rem;
                margin-top:12rem !important;
                .logo {
                    text-align: left;
                    img {
                        width: 50%;
                    }
                }
                .info {
                    text-align: left;
                    font-family: "Lato";
                    font-size: 14px;
                    ul {
                        list-style-type: none;
                        padding:0;
                        padding-left: 10px;
                        h6{
                            text-transform: uppercase;
                            font-weight: bold;
                        }
                        
                    }
                }
            }
            .footerBottomCopyright{
                padding: 0;
                line-height: 3rem;
                font-family: "Lato";
                font-size: 14px;
                border-top: 1px solid gainsboro;
                .left {
                    padding:0;
                    text-align: left !important;
                }
                .right{
                    padding: 0;
                    text-align: right !important;
                    img {
                        width: 24px;
                        height: 24px;
                    }
                }
                
            }
            
        }
    }

    @media screen and (max-width: 375px) {
        footer {
            .footerTop {
                height: 100vh;
                min-height: 600px;
                padding: 2rem 2rem;
                h1 {
                    font-size: 30px;
                }
                p{
                    padding: 0 !important;
                }
                .footerImg{
                    position: static;
                    margin-top: 40px;
                    img {
                        width: 100%;
                    }
                }
                .changePage {
                    display: block;
                    font-size: 40px;
                    width: 100%;
                    padding: 0 15px;
                     a{
                        display: inline-block;
                        padding:15px 55px;
                        background-color: gray;
                        border: 1px solid gray;
                        border-radius: 10px;
                        margin-top: 5px 0;
                        &.next {
                            margin-left: 5px;
                        }
                        &.previous {
                            margin-right: 5px;
                        }
                    }
                }
            }

            .footerBottom{
                height: 100vh;
                min-height: 600px;
                .footerBottomContact{
                    margin-top: 3rem !important;
                    .logo {
                        text-align: center;
                        padding-bottom: 3rem;
                    }
                    .info {
                        text-align: center;
                    }
                }
                .footerBottomCopyright{
                    margin-top: 5rem !important;
                    border-top: 1px solid gainsboro;
                    div {
                        width: 50%;
                    }
                }
            }
        }
        
    }
</style>

