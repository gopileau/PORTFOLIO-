<template>
    <div class="not-found-container">
      <img src="path/to/your/404-image.png" alt="404" />
      <h1>404</h1>
      <p>Page not found.</p>
    </div>
  </template>
  
  <style scoped>
  .not-found-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    background-color: #f2f2f2;
  }
  
  .not-found-container img {
    width: 300px;
    margin-bottom: 20px;
  }
  
  .not-found-container h1 {
    font-size: 96px;
    font-weight: bold;
    color: #333;
    margin-bottom: 10px;
  }
  
  .not-found-container p {
    font-size: 24px;
    color: #666;
  }
  </style>