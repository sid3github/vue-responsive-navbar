 <template>
    <div class="banner-section">
        <h1>Hello Tam</h1>
        <p>Have a nice day at work 😄</p>
        <div class="banner-button-section">
            <div class="banner-btns">
                <div class="pro-btn">
                    <button>Your Pro</button>
                    <button>Your Portfolio</button>
                </div>
                <div class="more-btn">
                    <button><i class="fas fa-ellipsis-h"></i></button>
                </div>
            </div>
            <div class="banner-box">
                <img src="../assets/banner-img.svg" alt="banner-image" />
                <div class="banner-content">
                    <div class="banner-content-img">
                        <i class="fas fa-history"></i>
                    </div>
                    <div class="banner-content-text">
                        <p>Renew your Pro Account</p>
                        <p>$99.00 for an additional year</p>
                    </div>
                    <div class="banner-content-btn">
                        <button>Renew Account</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "BannerSection",
};
</script>

<style>
.banner-section {
    padding: 15px;
}
.banner-section h1 {
    font-size: 42px;
}

.banner-section p {
    color: grey;
}

.banner-btns {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 40px 0 20px;
}

.pro-btn button {
    cursor: pointer;
    padding: 12px 6px;
    border-radius: 10px;
    border: none;
    width: 125px;
    outline: none;
    font-size: 10px;
}

.more-btn button {
    cursor: pointer;
    padding: 12px 6px;
    border-radius: 10px;
    border: none;
    width: 35px;
    outline: none;
    font-size: 10px;
    background: #fff;
    box-shadow: 0px 6px 6px #d1d1d1;
}

.pro-btn button:nth-child(1) {
    background: #5a5aa5;
    color: #fff;
}
.pro-btn button:nth-child(2) {
    background: #fff;
    color: grey;
}

.banner-box {
    width: 100%;
}

.banner-box img {
    width: 100%;
    background: rgb(234 235 255);
}

.banner-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #464678;
    position: relative;
    top: -6px;
}
</style>