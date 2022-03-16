<template>
    <div class="search-section">
        <div class="search">
            <input type="text" class="searchTerm" placeholder="Search..." />
            <button type="submit" class="searchButton">
                <i class="fa fa-search"></i>
            </button>
        </div>
        <div class="notify">
            <i class="fas fa-envelope-open-text"></i>
        </div>
        <div class="profile-img">
            <i class="fas fa-user-circle"></i>
        </div>
    </div>
</template>

<script>
export default {
    name: "SearchSection",
};
</script>

<style>
.search-section {
    width: 50%;
    margin: 0 auto;
    margin-right: initial;
    display: flex;
    align-items: center;
}

.search {
    display: flex;
    cursor: pointer;
    padding: 12px 6px;
}

.searchTerm {
    border: none;
    border-right: none;
    padding-left: 10px;
    border-radius: 12px 0 0 12px;
    outline: none;
    color: #9dbfaf;
    font-size: 10px;
}

.searchButton {
    width: 40px;
    height: 36px;
    border: none;
    background: #fff;
    text-align: center;
    color: #7272ff;
    border-radius: 0 12px 12px 0;
    cursor: pointer;
    font-size: 16px;
    padding-right: 10px;
}

.notify {
    margin-left: 6rem;
}
.profile-img {
    margin-left: 4rem;
}
</style>