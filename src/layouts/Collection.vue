<template>
    <div class="container-fluid collection">
        <CollectionElemt v-for="collection in collections" v-bind:key="collection.id" v-bind:collection="collection"/>
    </div>
</template>

<script>
import CollectionElemt from "../components/CollectionElemt"
export default {
    name: "Collection",
    components: {
        CollectionElemt,
    },
    data(){
    return {
      collections: [
        {
          id: 1,
          url: "Donata_13Mar197760.jpg",
          title: "CITY SLEEK",
          content: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
        },
        {
          id: 2,
          url: "Donata_13Mar197740.jpg",
          title: "RAW MODEL",
          content: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
        },
        {
          id: 3,
          url: "Donata_13Mar197788.jpg",
          title: "ART MODEL",
          content: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
        },
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
 .collection{
   padding:0;
 }
</style>
