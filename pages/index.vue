<template>
  <MainCard />
</template>

<script>
export default {
  name: "IndexPage",
};
</script>
<style >
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  color: #646464;
  font-family: "Anton", sans-serif;
}

.color-primary {
  color: #78cc6d;
}
.heading-style {
  font-size: 20px;
  font-weight: 600;
  min-height: 51px;
  padding: 1.5rem 2rem;
}
.pg-main {
  padding: 1.5rem 2rem;
}
.border-bottom {
  border-bottom: 0.7px ridge rgb(137, 132, 132, 0.5);
}
.color-main {
  color: #323232;
}
.color-link {
  color: #323232;
}
.color-link:hover {
  color: #65c18c;
}
.right-card-container {
  width: 56%;
  height: 600px;
  overflow-y: scroll;
  position: relative;
  background-color: #fff;
  z-index: 0;
  border-radius: 0 10px 10px 0;
}
.link_decoration {
  text-decoration: none;
  cursor: pointer;
}
@media screen and (min-width: 1900px) {
  .profile-container {
    height: 770px;
  }
  .right-card-container {
    height: 700px;
    width: 42%;
  }
  .left-width {
    width: 28%;
  }
}
@media screen and (max-width: 1435px) {
  .outer-background {
    flex-direction: column;
    height: auto;
  }
  .left-width {
    width: 50%;
    margin-bottom: 25px;
  }
  .right-card-container {
    border-radius: 10px;
    height: auto;
    width: 50%;
    margin-bottom: 25px;
  }
  .sidenav {
    position: fixed;
    top: 13%;
    left: 20%;
  }
  .slide {
    animation: none;
  }
  .social-contact {
    margin-top: 50px;
    margin-bottom: 20px;
  }
}
@media screen and (max-width: 1370px) {
  .left-width,
  .right-card-container {
    width: 55%;
  }

  .sidenav {
    left: 18%;
  }
}
@media screen and (max-width: 1240px) {
  .sidenav {
    left: 17.4%;
  }
  .table-design .value-style {
    float: none;
  }
}
@media screen and (max-width: 950px) {
  .sidenav {
    left: 14%;
  }
  .left-width,
  .right-card-container {
    width: 60%;
  }
}
@media screen and (max-width: 820px) {
  .value-style {
    float: none;
  }
}
@media screen and (max-width: 767px) {
  .sidenav {
    left: 12.5%;
  }
  .list-value-font {
    margin-top: 8px;
  }
  .box-element-contact {
    padding: 20px 0px;
    text-align: center;
  }
  .display-flex {
    flex-direction: column;
  }
  .width-50 {
    width: 100%;
  }
  .circle-background {
    flex-direction: row !important;
    margin-top: 10px;
  }
  .knowledge-alignment {
    flex-direction: row !important;
  }
  .title {
    margin-bottom: 15px;
  }

  .language:after {
    display: block;
  }
  .skills:after,
  .coding:after,
  .resume:after {
    display: none;
  }
}
@media screen and (max-width: 620px) {
  .box-style {
    width: 100%;
  }
  .table-design {
    flex-direction: column;
  }
  .left-width,
  .right-card-container {
    width: 100%;
  }
  .vertical-border:after {
    display: none;
  }
  .profile-container {
    margin-top: 136px;
  }
  .top-name {
    position: fixed;
    width: 100%;
    background-color: #fff;
    color: #000;
    top: 0;
    left: 0;
    z-index: 50;
    padding: 20px 40px;
    font-size: 25px;
    font-weight: 500;
    display: block;
  }
  .sidenav {
    top: 75px;
    left: 0;
    width: 100%;
    flex-direction: row !important;
    border-radius: 0px;
    border: none !important;
    padding-top: 5px;
  }
  .sidenav:after {
    content: "";
    position: absolute;
    width: 100%;
    height: 1px;
    left: 0;
    top: 5px;
    background: radial-gradient(
      ellipse at center,
      #3b3636 0%,
      rgba(255, 255, 255, 0) 80%
    );
  }
  .sidenav-element {
    position: relative;
  }
  .sidenav-element:after {
    content: "";
    position: absolute;
    width: 1px;
    height: 100%;
    left: 100%;
    background: radial-gradient(
      ellipse at top,
      #807e7e 0%,
      rgba(255, 255, 255, 0) 90%
    );
  }
}
@media screen and (max-width: 425px) {
  .outer-background {
    padding: 10px 10px;
  }
}
</style>

