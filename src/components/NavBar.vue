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
            console.log("showMenu", this.showMenu);
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
                        color: red;
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
                }
            }
        }
        .openMenu {
            display: none;
        }
    }

    @media screen and (max-width: 375px){
           .navbar{
               position: relative;
               .navbar-brand{
                   text-align: left;
                   img {
                       width: 30%;
                   }
               }
               ul {
                   display: none;
                   position: absolute;
                   top: 60px !important;
                   background-color: black;
                   opacity: 0.6;
                   width: 50%;
                   &#menuRight {
                       right: 0 !important;
                   }
                   &#menuLeft {
                       left: 0 !important;
                   }
                   li {
                       padding: 0 10px;
                       a{
                            color: white;
                       }
                   }

               }
                .openMenu {
                    display: block;
                    color: black;
                    cursor: pointer;
                    &:hover {
                        color: red;
                    }
                }
           }
    }
  
</style>
