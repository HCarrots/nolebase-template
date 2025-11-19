<template>
  <div class="links-container">
    <h1 class="title">友情链接</h1>
    <div class="links-list">
      <div
        class="link-item"
        v-for="(link, index) in links"
        :key="index"
      >
        <a :href="link.url" target="_blank">{{ link.name }}</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Links',
  data() {
    return {
      // 友情链接数据
      links: [
        { name: 'GitHub', url: 'https://github.com' },
        { name: 'Stack Overflow', url: 'https://www.stackoverflow.com' },
        { name: 'Reddit Programming', url: 'https://www.reddit.com/r/programming/' },
        { name: 'Mozilla', url: 'https://www.mozilla.org' },
        { name: 'Medium', url: 'https://www.medium.com' }
      ]
    };
  }
};
</script>

<style scoped>
.links-container {
  width: 80%;
  margin: 20px auto;
  padding: 20px;
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.title {
  text-align: center;
  color: #4CAF50;
}

.links-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.link-item {
  margin: 10px;
  padding: 10px 20px;
  background-color: #e7f4e4;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

.link-item:hover {
  background-color: #c0f2c0;
}

.link-item a {
  text-decoration: none;
  color: #333;
  font-size: 16px;
  font-weight: bold;
}

.link-item a:hover {
  color: #4CAF50;
}
</style>
