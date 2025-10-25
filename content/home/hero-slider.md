---
widget: markdown
headless: true
weight: 15

design:
  columns: '1'
  spacing:
    padding: ['0', '0', '0', '0']
  css_class: 'fullwidth-slider'
---

<div class="slider-container">
  <div class="slide active" style="background-image: url('https://images.unsplash.com/photo-1451187580459-43490279c0fa?w=1920&q=80');">
    <div class="slide-content">
      <h1>끊임없는 성장</h1>
      <p>DevOps와 자동화로 만드는 더 나은 내일</p>
      <a href="../contact/" class="btn btn-primary">함께하기</a>
    </div>
  </div>
  
  <div class="slide" style="background-image: url('https://images.unsplash.com/photo-1558494949-ef010cbdcc31?w=1920&q=80');">
    <div class="slide-content">
      <h1>데이터 중심의 세상</h1>
      <p>AWS와 Docker로 구축하는 효율적인 인프라</p>
      <a href="../project/" class="btn btn-primary">프로젝트 보기</a>
    </div>
  </div>
  
  <div class="slide" style="background-image: url('https://images.unsplash.com/photo-1519389950473-47ba0277781c?w=1920&q=80');">
    <div class="slide-content">
      <h1>클라우드 컴퓨팅의 미래</h1>
      <p>혁신적인 기술로 세상을 변화시키는 클라우드 여정</p>
      <a href="../about/" class="btn btn-primary">더 알아보기</a>
    </div>
  </div>
  
  <div class="slider-controls">
    <button class="prev" onclick="changeSlide(-1)">‹</button>
    <button class="next" onclick="changeSlide(1)">›</button>
  </div>
  
  <div class="slider-dots">
    <span class="dot active" onclick="currentSlide(1)"></span>
    <span class="dot" onclick="currentSlide(2)"></span>
    <span class="dot" onclick="currentSlide(3)"></span>
  </div>
</div>

<script>
let slideIndex = 1;
showSlide(slideIndex);

setInterval(() => {
  changeSlide(1);
}, 3000);

function changeSlide(n) {
  showSlide(slideIndex += n);
}

function currentSlide(n) {
  showSlide(slideIndex = n);
}

function showSlide(n) {
  let slides = document.querySelectorAll('.slide');
  let dots = document.querySelectorAll('.dot');
  
  if (n > slides.length) { slideIndex = 1 }
  if (n < 1) { slideIndex = slides.length }
  
  slides.forEach(slide => slide.classList.remove('active'));
  dots.forEach(dot => dot.classList.remove('active'));
  
  slides[slideIndex - 1].classList.add('active');
  dots[slideIndex - 1].classList.add('active');
}
</script>

<style>
/* 완전히 화면 전체 너비로 확장 */
body {
  overflow-x: hidden;
}

.home-section.fullwidth-slider,
section.fullwidth-slider {
  margin: 0 !important;
  padding: 0 !important;
  max-width: 100% !important;
  width: 100% !important;
}

.fullwidth-slider .container,
.fullwidth-slider > div {
  max-width: 100% !important;
  padding: 0 !important;
  margin: 0 !important;
  width: 100% !important;
}

.fullwidth-slider {
  width: 100% !important;
  margin: 0 !important;
  padding: 0 !important;
  position: relative !important;
}

.slider-container {
  position: relative;
  width: 100%;
  height: 350px;
  overflow: hidden;
  margin: 0;
  padding: 0;
}

.slide {
  position: absolute;
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
  display: none;
  align-items: center;
  justify-content: center;
}

.slide.active {
  display: flex;
  animation: fadeIn 1s;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.slide::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
}

.slide-content {
  position: relative;
  z-index: 2;
  text-align: center;
  color: white;
  padding: 2rem;
  max-width: 800px;
}

.slide-content h1 {
  font-size: 3rem;
  margin-bottom: 1rem;
  text-shadow: 2px 2px 4px rgba(0,0,0,0.7);
  font-weight: bold;
  white-space: nowrap;
}

.slide-content p {
  font-size: 1.3rem;
  margin-bottom: 1.5rem;
  text-shadow: 1px 1px 2px rgba(0,0,0,0.7);
}

.btn-primary {
  background-color: #2196F3;
  color: white;
  padding: 1rem 2.5rem;
  border-radius: 5px;
  text-decoration: none;
  display: inline-block;
  transition: all 0.3s;
  font-weight: 600;
  box-shadow: 0 4px 15px rgba(33, 150, 243, 0.4);
}

.btn-primary:hover {
  background-color: #1976D2;
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(33, 150, 243, 0.6);
}

.slider-controls button {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(255, 255, 255, 0.3);
  color: white;
  border: none;
  font-size: 3rem;
  padding: 0.5rem 1rem;
  cursor: pointer;
  z-index: 3;
  transition: all 0.3s;
  border-radius: 5px;
}

.slider-controls button:hover {
  background: rgba(255, 255, 255, 0.6);
  transform: translateY(-50%) scale(1.1);
}

.slider-controls .prev { left: 20px; }
.slider-controls .next { right: 20px; }

.slider-dots {
  position: absolute;
  bottom: 30px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 3;
}

.dot {
  display: inline-block;
  width: 14px;
  height: 14px;
  margin: 0 8px;
  background: rgba(255, 255, 255, 0.5);
  border-radius: 50%;
  cursor: pointer;
  transition: all 0.3s;
}

.dot.active, .dot:hover {
  background: white;
  transform: scale(1.4);
}

/* 모바일 반응형 */
@media (max-width: 768px) {
  .slider-container {
    height: 280px;
  }
  
  .slide-content h1 {
    font-size: 2rem;
    white-space: normal;
  }
  
  .slide-content p {
    font-size: 1.1rem;
  }
  
  .btn-primary {
    padding: 0.8rem 2rem;
    font-size: 0.9rem;
  }
  
  .slider-controls button {
    font-size: 2rem;
    padding: 0.3rem 0.7rem;
  }
}

/* 큰 화면 */
@media (min-width: 1200px) {
  .slider-container {
    height: 450px;
  }
  
  .slide-content h1 {
    font-size: 3.5rem;
  }
  
  .slide-content p {
    font-size: 1.5rem;
  }
}
</style>