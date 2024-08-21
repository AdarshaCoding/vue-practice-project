<template>
    <div class="app-header">
        <h4 class="app-title">App Title</h4>
        <div class="nav-bar">
            <ul class="list-items">
                <li>Home</li>
                <li>About</li>
                <li>Contact</li>
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
        name:"MainHeader" 
    }
</script>

<style>
.app-header{
    display: flex;
    justify-content: space-between;
    padding: 10px 10px;
    background-color: brown;
    color: white;
}

.app-title{
    cursor: pointer;
}
.nav-bar > .list-items {
    display: flex;
    list-style: none;
    cursor: pointer;
}
.nav-bar > .list-items > li {
    padding-left: 10px;

}
</style>