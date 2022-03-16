<template>
    <div class="main-container">
        <div class="sidenav" v-show="sideNav">
            <div class="sidenav-title">
                <h3>Interface</h3>
                <i class="fas fa-grip-horizontal"></i>
            </div>
            <div class="nav-links">
                <ul>
                    <li>
                        <i class="fas fa-th-large"></i>
                        <p>Dashboard</p>
                    </li>
                    <li>
                        <i class="fas fa-address-card"></i>
                        <p>Profile</p>
                    </li>
                    <li>
                        <i class="fas fa-tools"></i>
                        <p>Setting</p>
                    </li>
                    <li>
                        <i class="fas fa-cloud-upload-alt"></i>
                        <p>Cloud</p>
                    </li>
                    <li>
                        <i class="fas fa-comment-alt"></i>
                        <p>Message</p>
                    </li>
                </ul>
            </div>
            <div class="new-item-box">
                <div class="item-box">
                    <i class="fas fa-plus"></i>
                    <p>New Item</p>
                </div>
                <div class="item-box-content">
                    <p>Click '+' to create your new items</p>
                </div>
            </div>
        </div>
        <div class="content">
            <div class="hamburger-menu" @click="toggleMenu">
                <i class="fas fa-bars"></i>
            </div>
            <SearchSection />
            <div class="content-grid-section">
                <BannerSection />
                <DashboardSection />
            </div>
        </div>
    </div>
</template>

<script>
import SearchSection from "@/components/SearchSection.vue";
import BannerSection from "@/components/BannerSection.vue";
import DashboardSection from "@/components/DashboardSection.vue";
export default {
    name: "App",
    components: {
        SearchSection,
        BannerSection,
        DashboardSection,
    },
    data() {
        return {
            sideNav: true,
        };
    },
    created() {
        window.addEventListener("resize", this.checkScreen);
        this.checkScreen;
    },
    methods: {
        toggleMenu() {
            this.sideNav = !this.sideNav;
        },
        checkScreen() {
            if (window.innerWidth <= 915) {
                this.sideNav = false;
                return;
            }
            this.sideNav = true;
            return;
        },
    },
};
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Poppins", sans-serif;
}

body {
    background: rgb(248, 239, 241);
}

.main-container {
    display: grid;
    grid-template-columns: 15% auto;
    background: #fff;
    width: 95vw;
    height: 95vh;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    border-radius: 18px;
}

.content {
    margin: 5px;
    border-radius: 14px;
    background: #f4f4fc;
}

.fa-grip-horizontal {
    border-radius: 50%;
    background: #ebebf8;
    padding: 6px;
    font-size: 18px;
}

.sidenav-title {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 14px;
    margin: 20px 20px 40px 20px;
}

.nav-links {
    width: 125px;
    margin: 0 auto;
}

.nav-links ul li {
    display: flex;
    align-items: center;
    list-style: none;
    margin: 8px auto;
    cursor: pointer;
    padding: 12px 6px;
}

.nav-links ul li:hover {
    background: rgb(248, 239, 241);
    border-radius: 14px;
}

.nav-links li p {
    margin-left: 24px;
    color: grey;
    font-size: 12px;
}

.nav-links li p:hover {
    color: #000;
    font-weight: bold;
}

.fas {
    color: #8787fd;
}

.new-item-box {
    background: #f9f9fe;
    padding: 15px 20px;
    border-radius: 14px;
    margin: 0 auto;
    margin-left: 4px;
}

.item-box {
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    list-style: none;
    margin: 8px auto;
    padding: 12px 6px;
    color: #000;
    font-size: 12px;
    font-weight: bold;
    background: rgb(234 235 255);
    border-radius: 14px;
}

.item-box-content {
    margin: 20px auto;
}

.item-box-content p {
    font-size: 10px;
    text-align: center;
    color: grey;
}

.content-grid-section {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 1rem;
    margin: 5px 20px;
}

.hamburger-menu {
    display: none;
}

@media screen and (max-width: 915px) {
    .main-container {
        display: unset;
        grid-template-columns: unset;
    }

    .hamburger-menu {
        display: unset;
        padding: 15px;
    }

    .search-section {
        width: unset;
        margin-right: unset;
        justify-content: center;
    }

    .content-grid-section {
        display: unset;
    }

    /* .sidenav {
        display: none;
    } */
}
</style>
