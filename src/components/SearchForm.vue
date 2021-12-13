<template>
    <div class="d-flex ">
        <input 
        class="form-control mt-2 pt-1 pb-0 border-0 shadow-none" 
        v-model="message" 
        placeholder="Search shoes..."
        />
        <button type="submit"
        class="btn mt-3 shadow-none">
        <img class="desk"  src="../assets/magnifier.png" alt="magnifier icon">
        </button>
    </div>
    
</template>

<script>
export default {
    name: "SearchForm",

}

</script>

<style scoped lang="scss">
@media (min-width: 767.99px){
    .desk{
        width: 19px;
        height: 19px;
    }
}

</style>