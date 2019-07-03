<template>
    <footer class="container-fluid">
        <div class="row footerTop">
            <div class="col-md-6">
                <h1>#DONATALIFESTYLE</h1>
            </div>
            <div class="col-md-6">
                <p>Sed vulputate lorem ut bibendum elementum. Phasellus placerat elit arcu, at imperdiet augue ullamcorper id. Maecenas malesuada leo libero. </p>
            </div>
        </div>

        

        <div class="row footerBottom">
            <div class="container-fluid">
                <div class="row footerImg">
                    <div class="col-md-4">
                        <img src="../assets/02-Lifestyle-photos/Donata_13Mar197766.jpg"/>
                    </div>
                    <div class="col-md-4">
                        <img src="../assets/02-Lifestyle-photos/Donata_13Mar197838.jpg"/>
                    </div>
                    <div class="col-md-4">
                        <img src="../assets/02-Lifestyle-photos/Donata_13Mar197791.jpg"/>
                    </div>
                </div>
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
}
</script>

<style lang="scss" scoped>
    footer {
        padding: 0;
        height: 100vh;
        min-height: 600px;
        position: relative;
        .footerTop {
            background-color: black;
            color: white;
            padding: 3rem 3rem 15rem;
            h1 {
                text-transform: uppercase;
            }
            p{
                text-align: left;
            }
        }
        
        .footerBottom {
            margin: 12rem 3rem 0rem !important;
            position: absolute;
            top:0;
            left:0;
            right:0;
            .footerImg{
                left:0;
                right: 0;
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
            .footerBottomContact{
                border-bottom: 1px solid gainsboro;
                padding-bottom: 5rem;
                margin-top:5rem !important;
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
</style>

