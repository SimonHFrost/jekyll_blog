---
layout: home
list_title: 'Latest Posts'
---

<style>
.profile-container {
    display: flex;
    align-items: center;
    margin-bottom: 16px;
}

.profile-container img {
    border: 2px solid;
    max-width: 100000px;
    margin-right: 16px;
}

.profile-container .profile-image {
    text-align: center;
}

.location-text {
  margin-bottom: 0;
}

.profile-details {
    margin-bottom: 16px;
}

@media (max-width: 768px) {
    .profile-container {
        flex-direction: column;
        align-items: center;
        text-align: center;
    }

    .profile-container div {
        margin-left: 0;
    }

    .profile-details {
        display: flex;
        flex-direction: column;
    }
}
</style>

<div class="profile-container">
    <div class="profile-image">
        <img height="180px" width="180px" src="/assets/profile-picture.jpg" alt="Profile Picture"/>
        <p class="location-text"></p>
    </div>

    <div>
        <div class="profile-details">
            <span>📍🇲🇽 Mexico City (CST)</span>
        </div>
        <p>Freelance Full Stack Engineer interested in technology, start-ups, design, and community. This is my blog.</p>
    </div>
</div>
<div class="header-colors">
    <div class="color1"></div>
    <div class="color2"></div>
    <div class="color3"></div>
</div>
