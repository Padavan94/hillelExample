<template>
    <form action="">
        <div>
            Step 1
            <label for=""><input type="radio"> step 1.1</label>
            <label for=""><input type="radio"> step 1.2</label>
        </div>
        <div>
            step 2
        </div>

    </form>
</template>

<script>
    export default {
        name: "registration-form",

        data: function () {
            return {
                sportsman: false,
                federation: true
            }
        }
    }
</script>

<style scoped>

</style>