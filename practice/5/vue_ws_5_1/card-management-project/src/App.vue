<template>
  <div id="app">
    <header>
      <h1>Header 영역</h1>
      <p>여기에 헤더 내용을 작성하세요.</p>
    </header>

    <main>
      <h2>Main 영역</h2>
      <p>여기에 메인 콘텐츠를 작성하세요.</p>
    </main>

    <article>
      <h3>Article 영역</h3>
      <p>여기에 아티클 내용을 작성하세요.</p>
    </article>

    <footer>
      <h4>Footer 영역</h4>
      <p>여기에 푸터 내용을 작성하세요.</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style scoped>
#app {
  text-align: center;
}

header, main, article, footer {
  padding: 20px;
  margin: 10px;
  border: 1px solid #ddd;
  border-radius: 8px;
}

header {
  background-color: #f5f5f5;
}

main {
  background-color: #e9f7ef;
}

article {
  background-color: #fff3e0;
}

footer {
  background-color: #fbe9e7;
}
</style>
