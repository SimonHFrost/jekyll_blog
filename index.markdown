---
layout: home
list_title: "Latest Posts"
---

<style>
.profile-container {
    display: flex;
    align-items: center;
    margin-bottom: 16px;
}

.profile-container img {
    border: 2px solid #778183;
    max-width: 100000px;
    margin-right: 16px;
}

.profile-summary > p:last-child {
    margin-bottom: 0px;
}

@media (max-width: 768px) {
    .profile-summary > p:last-child {
        margin-bottom: 16px;
    }

    .mobile-only {
        display: block;
    }

    .desktop-only {
        display: none;
    }

    .profile-container {
        margin-bottom: 0;
    }

    .profile-container img {
        margin: 0px;
        margin-bottom: 16px;
    }
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

    .fade-in {
      opacity: 0;
      transition: opacity 0.3s ease-out;
    }

    .fade-in.visible {
      opacity: 1;
    }
}
</style>

<script>
    document.addEventListener('DOMContentLoaded', () => {
    function fadeIn() {
      const image = document.getElementsByClassName('profile-image')[0];
      image.classList.add('visible');
    }

      fadeIn();
    });
</script>

<div class="profile-container">
    <div class="profile-image fade-in">
        <img height="180px" width="180px" src="/assets/profile-picture.jpg" alt="Profile Picture"/>
        <!-- <p class="location-text">Mexico City, Mexico</p> -->
    </div>

    <div class="profile-summary">
        <p class="mobile-only">✉️ simonhfrost(at)gmail.com</p>
        <p style="margin-bottom: 0; font-weight: bold;">Freelance Frontend Engineer</p>
        <p>Interested in LLMs, start-ups, design, and community.</p>
    </div>

</div>
