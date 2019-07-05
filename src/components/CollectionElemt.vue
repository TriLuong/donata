<template>
    <div class="container-fluid collectionElemt">
        <div class="row bgColl">
            <img v-bind:src="require('../assets/02-Lifestyle-photos/' + collection.url)" />
            <div class="blurColor" />
        </div>
        <div class="row infoColl">
            <div class="col-md-7 col-xs-12 infoCollLeft">
                <p>Collection {{collection.id}}</p>
                <h1>{{collection.title}}</h1>
                <p>{{collection.content}}</p>
            </div>
            <div class="col-md-5 col-xs-12 infoCollRight">
                <div class="eventDetail">
                    <a href="#">EVENT DETAILS &rarr;</a>
                </div>
                
            </div>
        </div>
    </div>

</template>

<script>
export default {
    name: "CollectionElemt",
    props: {
        collection: Object,
    },
}
</script>

<style lang="scss" scoped>
    .collectionElemt{
        padding:0;
        position: relative;
        .bgColl{
            img {
                width: 100%;
                min-height: 600px;
                height: 100vh;
                transform: scaleX(-1);
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
        };
        .infoColl {
            color: white;
            position: absolute;
            bottom: 2rem;
            left:0;
            right:0;
            .infoCollLeft {
                text-align: left;
                padding: 0 5rem;
            }
            .infoCollRight {
                position: relative;
                .eventDetail{
                    position: absolute;
                    font-family: "Lato";
                    font-weight: bold;
                    bottom:1rem;
                    left:0;
                    right:0;
                    a{
                        color: white;
                        text-decoration: none;
                        padding: 10px;
                        &:hover {
                            background-color: gainsboro;
                            color: black;
                            border-radius: 10px;
                        }
                    }
                    
                }
            }
        }
    }

    @media screen and (max-width: 375px) {
        .collectionElemt{
            .bgColl{
                img {
                    object-fit: cover;
                }
                .blurColor {
                    height: 70vh;
                }
            }
            .infoColl {
                .infoCollLeft {
                    padding-left: 2rem;
                }
                .infoCollRight {
                    .eventDetail{
                        position: static;
                        text-align: left;
                        padding-left: 1rem;
                    }
                }
            }
        }
    }
</style>

