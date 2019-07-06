<template>
    <div class="container-fluid eventLayout">
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
.eventLayout {
    padding:0;
    height: 100vh;
    min-height: 600px;
    @media screen and (max-width: 736px) {
        min-height: 350px;
    }
}
</style>

