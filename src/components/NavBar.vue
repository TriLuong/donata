<template>
    <div class="container navBar">
        <nav class="navbar navbar-expand-sm">
            <!-- Links -->
            <ul class="navbar-nav">
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
            <ul class="navbar-nav">
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
        </nav>
    </div>
</template>

<script>
export default {
    name: "NavBar"
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
                width: 18%;
            }
        }
        ul{
            align-content: flex-end;
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
    }
  
</style>
