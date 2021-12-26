<template>
<div class="presentation">
      <div class="titre">
        <h1>More than just shorterlinks</h1>
        <h2>
          Build your brand's recognition and get detailed insights on how your
          links are performing.
        </h2>
        <div class="calltoaction">Get started</div>
      </div>
      <img
        src="../assets/illustration-working.svg"
        alt=""
        class="illustration"
      />
    </div>
</template>

<script>
export default {
name:"pres",
}
</script>

<style>
.calltoaction {
  width: max-content;
  padding: 10px 30px;
  background: var(--primary);
  border-radius: 25px;
  color: white;
  font-weight: 500;
  margin-top : 50px;
  font-family: "Poppins";
  font-size: 1em;
}
.presentation{
      display: flex;
    position: relative;
    margin-top: 50px;
    align-items: center;
}
.illustration {
  width: 50%;
  position: relative;
  left: 15%;
}
</style>
