<template>
<header class="main-menu bg-pattern">
  <div class="container-fluid h-100">
    <nav class="nav justify-content-between">
      <a class="nav-link active brand-logo" href="#">
        <p class="brand-text">Deeply</p>
      </a>
      <a class="nav-link" href="#">Contact</a>
    </nav>
  </div>
</header>
</template>
<script>
</script>

<style lang="scss">
  @import "../styles/partials/_colors.scss";
  @import "../styles/partials/_fonts.scss";
  .main-menu {
    background-color: $primario;
    // background-color: map-get($colors, primario );
    // background-image: url('../assets/img/pattern_positive.png');
    // background-blend-mode: multiply;
    height: 25vh;
    .nav {
      height: 50%;
      font-family: $stylish_reg;
      display: flex;
      align-items: center;
      .nav-link {
        color: $white;
        letter-spacing: .1em;
      }
    }
  }
</style>

