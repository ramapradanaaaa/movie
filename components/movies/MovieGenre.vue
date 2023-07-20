<template>
  <div class="featured__controls">
    <ul>
      <li>All</li>
      <li>Actions</li>
      <li>Science Fiction</li>
      <li>Horror</li>
      <li>Thriller</li>
      <li>Comedy</li>
      <li>Romance</li>
      <li>Adventure</li>
      <li>Fantasy</li>
    </ul>
  </div>
</template>

<style scoped>
.featured__controls {
  text-align: center;
  margin-bottom: 50px;
}

.featured__controls ul li {
  list-style: none;
  font-size: 18px;
  color: #1c1c1c;
  display: inline-block;
  margin-right: 25px;
  position: relative;
  cursor: pointer;
}

.featured__controls ul li.active:after {
  opacity: 1;
}

.featured__controls ul li:after {
  position: absolute;
  left: 0;
  bottom: -2px;
  width: 100%;
  height: 2px;
  background: #7fad39;
  content: "";
  opacity: 0;
}

.featured__controls ul li:last-child {
  margin-right: 0;
}
</style>