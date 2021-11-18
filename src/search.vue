<template>
  <div>
    <h4 class="search">
      <nav class="navbar navbar-light bg-light">
        <div class="container-fluid">
          <form class="d-flex">
            <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
            <button class="btn btn-outline-success" type="submit">Search</button>
          </form>
        </div>
      </nav>
    </h4>
  </div>
</template>

<script>
export default {
  name : 'search',
}
</script>

<style>
.search {
  background: #eee;
  padding: 10px;
  margin: 10px;
  border-radius: 5px;
  text-align: center;
}
</style>
