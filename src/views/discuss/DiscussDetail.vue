<template>
    <div class="d-wrapper">
      <div class="d-header">
        <div class="d-title">Tiều đề: {{ data.ThreadName }}</div>
        <p>
          <span class="author">Người đăng:</span>
          <span>{{ data.ThreadUser }}</span>
        </p>
        <p class="desc">
          "Em cần sắp xếp dòng code. Em cần sắp xếp dòng code. Em cần sắp xếp dòng
          code. Em cần sắp xếp dòng code."
        </p>
      </div>
      <div class="btn-answer">
        <button class="icon-button btn create">
          <p class="btn-label">Trả lời</p>
        </button>
      </div>
      <div class="d-content">
        <div class="d-item">
          <div class="item-top">
            <span class="item-name">Nguyễn Trọng Tuế</span>
            <span class="item-time">({{ new Date().toLocaleDateString() }})</span>
          </div>
          <p class="item-desc">Sử dụng thuộc tính flex-wrap thử xem bạn.</p>
        </div>
        <div class="d-item">
          <div class="item-top">
            <span class="item-name">Nguyễn Trọng Tuế</span>
            <span class="item-time">({{ new Date().toLocaleDateString() }})</span>
          </div>
          <p class="item-desc">Sử dụng thuộc tính flex-wrap thử xem bạn.</p>
        </div>
        <div class="d-item">
          <div class="item-top">
            <span class="item-name">Nguyễn Trọng Tuế</span>
            <span class="item-time">({{ new Date().toLocaleDateString() }})</span>
          </div>
          <p class="item-desc">Sử dụng thuộc tính flex-wrap thử xem bạn.</p>
        </div>
      </div>
      <div class="btn-back">
      <button class="icon-button btn create" @click="onBack()">
        <p class="btn-label">Quay lại</p>
      </button>
    </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "DiscussDetail",
    props: ["data"],
    methods: {
        onBack(){
            this.$emit("back")
        }
    }
  };
  </script>
  
  <style scoped>
  .d-header {
    padding-bottom: 24px;
    border-bottom: 1px solid #ccc;
  }
  .d-wrapper {
    background-color: white;
    padding: 24px;
    border-radius: 4px;
    margin-top: 16px;
    height: calc(100% - 24px);
    margin-bottom: 24px;
  }
  .d-title {
    font-size: 24px;
    font-weight: 700;
  }
  p {
    font-size: 16px;
    margin: 10px 0;
  }
  .author {
    text-decoration: underline;
    font-weight: 600;
  }
  .desc {
  }
  .btn-answer {
    margin-top: 16px;
    display: flex;
    justify-content: flex-end;
  }
  .icon-button {
  }
  .btn-label {
  }
  .d-content {
  }
  .d-item p {
    margin: 0;
  }
  .d-item {
    margin: 8px 0;
  }
  .item-top {
  }
  .item-name {
    color: green;
    font-weight: 700;
    margin-right: 8px;
    font-size: 14px;
  }
  .item-time {
    font-size: 14px;
  }
  .item-desc {
    font-size: 14px;
  }
  </style>