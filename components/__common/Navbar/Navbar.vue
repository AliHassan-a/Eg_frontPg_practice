<template>
    <div class="navbar_container">
        <div class="wrapper">
            <!-- Mobile View Navbar -->
            <div class="mobile_header">
                <div class="logo">
                    <NuxtLink>
                        <img src="../../../assets/HomePage/EG EnergyGigs logo.svg" alt="">
                    </NuxtLink>

                </div>

                <div class="sidebar_toggle" @click="mobileMenu" v-if="!toggleValue">
                    <div class="horizontal_bar"></div>
                    <div class="horizontal_bar"></div>
                    <div class="horizontal_bar"></div>
                </div>
            </div>
            <div v-if="toggleValue" :class="{ 'mobile_nav': true, active: toggleValue }">
                <div class="close_btn" @click="mobileMenu">
                    <div class="close_icon">X</div>
                </div>
                <ul class="mobile_menu">
                    <li class="menu_item">
                        Who's using us
                    </li>
                    <li class="menu_item">Testimonials</li>
                    <li class="menu_item">Services we offer</li>
                    <li class="menu_item">How it works</li>
                </ul>
            </div>
            <!-- Mobile View Navbar -->
            <!-- Desktop View Navbar -->
            <div class="desktop_header">
                <div class="left_side">
                    <div class="desktop_logo">
                        <img src="../../../assets/HomePage/EGDesktop.svg" alt="">
                    </div>
                    <div class="desktop_items">
                        <ul>
                            <li>Who's using us </li>
                            <li>Testimonials</li>
                            <li>Services we offer</li>
                            <li>How it works</li>
                        </ul>
                    </div>

                </div>
                <div class="right_side">
                    <button class="btn">Sign In</button>
                    <button class="btn">Sign Up</button>
                </div>

            </div>
            <!-- Desktop View Navbar -->



        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            toggleValue: false
        }
    },
    methods: {
        mobileMenu() {
            this.toggleValue = !this.toggleValue
        }
    }
}
</script>
<style lang="scss" scoped src="./navbar.scss"></style>