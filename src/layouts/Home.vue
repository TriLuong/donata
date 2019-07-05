<template>
    <div class="container-fluid homePage">
        <div class="bgHomePage">
            <img src="../assets/02-Lifestyle-photos/Donata_13Mar197798.jpg"/>
        </div>
        <NavBar />
        <div class="blurColor" />

        <div class="slogan">
            <h1>LIFESTYLE WITHOUT BORDERS</h1>
            <a href="#">GET IN TOUCH &rarr;</a>
        </div>
        
    </div>
</template>

<script>
import NavBar from "../components/NavBar"
export default {
    name: "Home",
    components: {
        NavBar,
    }
}
</script>
<style lang="scss" scoped>
    .homePage {
        padding: 0 !important;
        position: relative;
        height: 100vh;
        min-height: 600px;
        .bgHomePage{
            img {
                object-fit: fill;
                width: 100%;
                min-height: 600px;
                height: 100vh;
            }
        }
        .navBar {
            position: absolute;
            top: 0;
            left:0;
            right: 0;
        }
        .slogan{
            position: absolute;
            bottom: 5%;
            left:0;
            right: 0;
            h1 {
                text-transform: uppercase;
                text-shadow: 0 2px 4px rgba(0, 0, 0, 0.35);
                font-size: 40px;
                font-weight: bold;
                font-style: normal;
                font-stretch: normal;
                line-height: 1.2;
                text-align: center;
                color: white;
            }
            a{
                text-transform: uppercase;
                text-decoration: none;
                font-size: 16px;
                font-weight: bold;
                font-style: normal;
                font-stretch: normal;
                line-height: 1.5;
                letter-spacing: 1px;
                cursor: pointer;
                color:white;
                padding:10px;
                &:hover {
                    background-color: gainsboro;
                    color: black;
                    border-radius: 10px;
                }
            }
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
    }

    @media screen and (max-width: 375px) {
        .homePage {
            .bgHomePage{
                img {
                    object-fit: cover;
                    width: 100%;
                }
            }
            .slogan{
                h1 {
                    color: white;
                    width: 50%;
                    margin:0 auto;
                    margin-bottom: 1rem;
                }
            }
        }
    }
</style>

