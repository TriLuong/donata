<template>
    <div class="container-fluid collectionElemt">
        <div class="row bgColl">
            <div class="col-md-12">
                <img v-bind:src="require('../assets/02-Lifestyle-photos/' + collection.url)" />
            </div>
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
            };
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
                a{
                    color: white;
                    text-decoration: none;
                }
                .eventDetail{
                    position: absolute;
                    font-family: "Lato";
                    bottom:1rem;
                    left:0;
                    right:0;
                    a:hover {
                        color:red;
                    }
                }
            }
        }
    }
</style>

