<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    active: false
                },
                {
                    text: "COMICS",
                    url: "#",
                    active: true
                },
                {
                    text: "MOVIES",
                    url: "#",
                    active: false
                },
                {
                    text: "TV",
                    url: "#",
                    active: false
                },
                {
                    text: "GAMES",
                    url: "#",
                    active: false
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    active: false
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    active: false
                },
                {
                    text: "FANS",
                    url: "#",
                    active: false
                },
                {
                    text: "NEWS",
                    url: "#",
                    active: false
                },
                {
                    text: "SHOP",
                    url: "#",
                    active: false
                }
            ],
        }
        
    }
}
</script>

<template>
  <header>
    <div class="container">
        <div>
            <img src="../assets/dc-logo.png" alt="image">
        </div>
    
        <div class="nav-head">
            <ul>
                <li class="li-nav" v-for="link in links" :class="{ active: link.active}"><a :href="link.url">{{ link.text }}</a></li>
            </ul>
        </div>   
    </div>
  </header>
</template>

<style scoped lang="scss">
@use "../style/partials/variables.scss" as *;

header {
    @include mixin.flex;
    @include mixin.margin;
}
.container {
    height: 150px;
    background-color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;

    &:hover {
        color: #0C7CEC;
        border-bottom: 2px solid #0C7CEC;
    }
}
.li-nav a{
    color: grey;
    font-weight: bold;
    text-decoration: none;
}

ul {
    display: flex;
    gap: 20px;
    list-style: none;
}
</style>