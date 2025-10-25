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
      <h1>클라우드 컴퓨팅의 미래</h1>
      <p>혁신적인 기술로 세상을 변화시키는 클라우드 여정</p>
      <a href="../about/" class="btn btn-primary">더 알아보기</a>
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
      <h1>끊임없는 성장</h1>
      <p>DevOps와 자동화로 만드는 더 나은 내일</p>
      <a href="../contact/" class="btn btn-primary">함께하기</a>
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
/* 화면 꽉 차게 만들기 */
.fullwidth-slider {
  margin: 0 !important;
  padding: 0 !important;
  width: 100vw !important;
  position: relative;
  left: 50%;
  right: 50%;
  margin-left: -50vw !important;
  margin-right: -50vw !important;
}

.slider-container {
  position: relative;
  width: 100%;
  height: 70vh;  /* 화면 높이의 70% */
  min-height: 500px;  /* 최소 높이 */
  max-height: 800px;  /* 최대 높이 */
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
  font-size: clamp(2rem, 5vw, 3.5rem);  /* 반응형 폰트 */
  margin-bottom: 1rem;
  text-shadow: 2px 2px 4px rgba(0,0,0,0.7);
  font-weight: bold;
}

.slide-content p {
  font-size: clamp(1rem, 3vw, 1.5rem);  /* 반응형 폰트 */
  margin-bottom: 2rem;
  text-shadow: 1px 1px 2px rgba(0,0,0,0.7);
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
  transition: background 0.3s;
  border-radius: 5px;
}

.slider-controls button:hover {
  background: rgba(255, 255, 255, 0.5);
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
  width: 15px;
  height: 15px;
  margin: 0 8px;
  background: rgba(255, 255, 255, 0.5);
  border-radius: 50%;
  cursor: pointer;
  transition: all 0.3s;
}

.dot.active, .dot:hover {
  background: white;
  transform: scale(1.2);
}

/* 모바일 반응형 */
@media (max-width: 768px) {
  .slider-container {
    height: 60vh;
    min-height: 400px;
  }
  
  .slide-content h1 {
    font-size: 2rem;
  }
  
  .slide-content p {
    font-size: 1rem;
  }
  
  .slider-controls button {
    font-size: 2rem;
    padding: 0.3rem 0.7rem;
  }
}
</style>
