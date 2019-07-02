<template>
    <div class="container-fluid event">
        <EventFirst />
    </div>
</template>

<script>
import EventFirst from "../components/EventFirst"
export default {
    name: "Event",
    components: {
        EventFirst,
    }
}
</script>
<style lang="scss" scoped>
    .event {
        padding:0;
    }
</style>

