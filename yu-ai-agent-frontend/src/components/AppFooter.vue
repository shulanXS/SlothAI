<template>
  <footer class="app-footer">
    <div class="footer-bottom">
      <p>© {{ currentYear }} 树懒AI超级智能体应用平台 - 让AI为你服务</p>
    </div>
  </footer>
</template>

<script setup>
import { computed } from 'vue'

// 计算当前年份
const currentYear = computed(() => new Date().getFullYear())
</script>

<style scoped>
.app-footer {
  background-color: #fff;
  padding: 40px 0 20px;
  color: #666;
  border-top: 1px solid #eee;
  width: 100%;
  margin-top: auto;
  position: relative;
  z-index: 2;
}

.footer-content {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 0 20px;
}

.footer-section {
  flex: 1;
  min-width: 200px;
  margin-bottom: 30px;
  padding: 0 15px;
}

.footer-logo h3 {
  font-size: 1.25rem;
  margin-bottom: 15px;
  color: #333;
}

.footer-section h4 {
  font-size: 1rem;
  margin-bottom: 15px;
  color: #333;
}

.footer-links {
  display: flex;
  flex-direction: column;
}

.footer-links a {
  margin-bottom: 10px;
  color: #666;
  text-decoration: none;
  transition: color 0.2s;
}

.footer-links a:hover {
  color: #007bff;
}

.qrcode {
  display: flex;
  align-items: center;
}

.qrcode-container {
  text-align: center;
}

.qrcode-placeholder {
  width: 90px;
  height: 90px;
  background-color: #f5f5f5;
  margin: 0 auto 10px;
  border-radius: 4px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2rem;
}

.qrcode-placeholder:after {
  content: '🤖';
}

.footer-bottom {
  text-align: center;
  padding-top: 20px;
  margin-top: 20px;
  border-top: 1px solid #eee;
  color: #999;
  font-size: 0.9rem;
}

/* 响应式设计 */
@media (max-width: 768px) {
  .footer-content {
    flex-direction: column;
  }
  
  .footer-section {
    width: 100%;
    margin-bottom: 20px;
    padding: 0;
  }
}

@media (max-width: 480px) {
  .app-footer {
    padding: 30px 0 15px;
  }
  
  .footer-section h4 {
    font-size: 0.95rem;
  }
  
  .footer-links a {
    font-size: 0.9rem;
  }
  
  .qrcode-placeholder {
    width: 80px;
    height: 80px;
  }
}
</style> 