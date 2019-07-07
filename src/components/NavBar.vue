<template>
    <div class="container navBar">
        <nav class="navbar navbar-expand-sm">
            <!-- Links -->
            <ul id="menuLeft" class="navbar-nav">
                <li class="nav-item">
                    <a class="nav-link" href="#">NEW</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">DINNING</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">LIVING</a>
                </li>
            </ul>

            <!-- Brand/logo -->
            <a class="navbar-brand" href="#">
                <img src="../assets/logo.svg"/>
            </a>
        
            <!-- Links -->
            <ul id="menuRight" class="navbar-nav">
                <li class="nav-item">
                    <a class="nav-link" href="#">BEDROOM</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">STORAGE</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">BAR</a>
                </li>
            </ul>
            <a class="openMenu" v-on:click="openNav">&#9776;</a>
        </nav>
    </div>
</template>

<script>
export default {
    name: "NavBar",
    data() {
        return {
            showMenu: false, 
        }
    },
    methods: {
        openNav: function(){
            var menuLeft = document.getElementById("menuLeft");
            var menuRight = document.getElementById("menuRight");
            var iconShowMenu = document.getElementsByClassName("openMenu")[0];
            if (!this.showMenu) {
                menuLeft.style.display="flex";
                menuRight.style.display="flex";
                iconShowMenu.innerHTML = "&times;"
            } else {
                menuLeft.style.display="";
                menuRight.style.display="";
                iconShowMenu.innerHTML = "&#9776;"
            }
            this.showMenu = !this.showMenu;
        }
    },
}
</script>

<style lang="scss" scoped>
    .navbar{
        font-family: "Lato";
        border-bottom: 1px solid gainsboro;
        .navbar-brand{
            flex: 50%;
            margin: 0 !important;
            img {
                width: 40%;
            }
        }
        ul{
            display: flex;
            li{
                &:hover {
                    a{
                        color: white;
                        background-color: gray;
                    }
                }
                a{
                    text-transform: uppercase;
                    font-size: 12px;
                    font-weight: bold;
                    font-style: normal;
                    font-stretch: normal;
                    line-height: 1.33;
                    letter-spacing: 2px;
                    color: black;
                    padding: 5px;
                }
            }
        }
        .openMenu {
            display: none;
        }
    }
    @media screen and (max-width: 736px) {
        .navbar{
               .navbar-brand{
                   position: relative;
                   text-align: left;
                   img {
                       width: 30%;
                   }
                }
                ul {
                    display: none;
                    position: absolute;
                    top: 65px;
                    background-color: gainsboro;
                    width: 50%;
                    opacity: 0.8;
                    &#menuRight {
                        right: 0 ;
                    }
                    &#menuLeft {
                        left: 0 ;
                    }
                    li {
                        padding: 0 5px;
                            &:hover {
                                a{
                                    color: white;
                                    background-color: gray;
                                }
                            }
                            a{
                                    color: black;
                            }
                    }

                }
                .openMenu {
                    display: block;
                    color: black;
                    cursor: pointer;
                    padding: 10px;
                    &:hover {
                        background-color: gainsboro;
                        color: black;
                        border-radius: 10px 0;
                    }
                }
           }
        }
    

    @media screen and (max-width: 414px){
           .navbar{
               ul {
                   top: 60px;
                   background-color: gainsboro;
                   li {
                       padding: 0 10px;
                   }

               }
           }
    }

    
  
</style>
