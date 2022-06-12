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
  font-family: "Roboto", sans-serif;
  /* background-image: url("~@/assets/img/back-img.png"); */
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
  width: 55%;
  height: 650px;
  overflow-y: scroll;
}
.link_decoration {
  text-decoration: none;
}
</style>

