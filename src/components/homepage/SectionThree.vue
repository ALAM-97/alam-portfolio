<template>
  <div class="page">
    <div class="page-content">
      <div class="left-content">
        <h2>Currently,</h2>
        <p>
          I work as a Freelancer and I’m crafting a Website for The Team, a
          young startup which provides sport trading online courses. The main
          goal is to build a platform easy to use that helps the users to buy
          the courses and, in the future, use the platform to see the courses.
        </p>
        <p>
          Before now, I was a Jr Full Stack Developer at Yeldo, an online
          platform that grants digital access to real estate investments for
          professional investors, where I worked mainly on the user dashboard
          and the admin backoffice.
        </p>
        <p>
          Prior to Yeldo, I was a React Developer in Runtheons, building the new
          Institutional website.
        </p>
      </div>
      <div class="right-content">
        <img alt="experience image" src="../../assets/img/experience-img.png" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionThree",
};
</script>

<style scoped lang="scss">
.page {
  color: #fff;
  background: linear-gradient(rgba(30, 30, 30, 0.9), rgba(30, 30, 30, 0.9)),
    url("../../assets/Logo.svg");
  background-color: #1e1e1e;
  background-repeat: no-repeat;
  background-position: center;
  background-size: 80%;
}
.page-content {
  .left-content,
  .right-content {
    width: 50%;
    color: #ffffff;
  }
  .left-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    position: relative;
    height: 100%;
    h2 {
      color: #fffd2a;
    }
    p {
      width: 85%;
    }
  }
  .right-content {
    align-self: center;
    margin-left: 12%;
  }
}
</style>
