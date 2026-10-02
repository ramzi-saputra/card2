<template>
  <nav class="navbar">
    <div class="logo">
      SMK Yadika soreang - Onlineshop
    </div>

  <div class="nav-menu">
     <RouterLink to="/"> Landing</RouterLink>
        <RouterLink to="/product"> Product</RouterLink>
        <RouterLink to="/About"> About</RouterLink>
        <RouterLink to="/Contact"> Contact</RouterLink>
        <RouterLink to="/FAQ"> FAQ</RouterLink>
  </div>
</nav>
</template>
<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-bottom: 20px;
  border-bottom: 1px solid #999;
}

.logo {
  color: #1f3b5b;
}
.nav-menu {
  display: flex;
  gap: 20px;
}
</style>