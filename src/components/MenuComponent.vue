<template>

<div class="menu">
    <p>Featured Categories</p>
     <div class="m">
            <p>All</p>
            <p>Milk</p>
            <p>Coffee&Teas</p>
            <p>Pet Food</p>
            <p>Meats</p>
            <p>Vegetables</p>
    <p>Fruits</p> 
     </div>
</div>
</template>
<script>
export default {
    
}
</script>
<style>
.menu{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-left: 20px;
    padding-right: 20px;
}
.m{
    display: flex;
    gap: 20px;

}
</style>