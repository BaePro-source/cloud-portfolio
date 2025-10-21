---
widget: slider
headless: true
weight: 15

design:
  # Slide height is automatic unless you force a specific height (e.g. '400px')
  slide_height: '500px'
  is_fullscreen: false
  # Automatically transition through slides?
  loop: true
  # Duration of transition between slides (in ms)
  interval: 3000

content:
  slides:
    - title: 클라우드 컴퓨팅의 미래
      content: '혁신적인 기술로 세상을 변화시키는 클라우드 여정'
      align: center
      background:
        image:
          filename: 'https://images.unsplash.com/photo-1451187580459-43490279c0fa?w=1920&q=80'
          filters:
            brightness: 0.5
        position: center
        color: '#000'
      link:
        icon: graduation-cap
        icon_pack: fas
        text: 더 알아보기
        url: ../about/
    
    - title: 데이터 중심의 세상
      content: 'AWS와 Docker로 구축하는 효율적인 인프라'
      align: center
      background:
        image:
          filename: 'https://images.unsplash.com/photo-1558494949-ef010cbdcc31?w=1920&q=80'
          filters:
            brightness: 0.5
        position: center
        color: '#111'
      link:
        icon: code
        icon_pack: fas
        text: 프로젝트 보기
        url: ../project/
    
    - title: 끊임없는 성장
      content: 'DevOps와 자동화로 만드는 더 나은 내일'
      align: center
      background:
        image:
          filename: 'https://images.unsplash.com/photo-1519389950473-47ba0277781c?w=1920&q=80'
          filters:
            brightness: 0.5
        position: center
        color: '#333'
      link:
        icon: rocket
        icon_pack: fas
        text: 함께하기
        url: ../contact/
---