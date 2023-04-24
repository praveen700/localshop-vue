<template>
    <div class="card">
        <div id="card-header">
            <slot name="header"></slot>
        </div>
        <div id="card-content" class="card-content">
            <h2>Card Title</h2>
                <slot>Default Content</slot>
            <a href="#" class="button">Read More</a>
            <div id="card-footer">
                <slot name="footer"></slot>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Card',
    
}
</script>

<style scoped>
.card {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  transition: 0.3s;
  width: 300px;
  margin: 20px;
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}

.card img {
  width: 100%;
  height: auto;
}

.card-content {
  padding: 10px;
}

.card h2 {
  font-size: 24px;
  margin-bottom: 10px;
}

.card p {
  font-size: 14px;
  margin-bottom: 10px;
}

.button {
  background-color: #4CAF50;
  color: white;
  padding: 8px 16px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 14px;
  margin-top: 10px;
  border-radius: 4px;
}

</style>