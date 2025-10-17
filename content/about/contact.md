---
# An instance of the Contact widget.
# Documentation: https://docs.hugoblox.com/getting-started/page-builder/
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 50

title: Contact
subtitle: 
sections:
  - block: contact
    content:
      title: Contact
      text: |-
        <br> <span style="font-size:95%">클라우드 컴퓨팅 혹은 클라우드 개발자 관련해 관심 있으시면 아래로 연락주시면 감사드리겠습니다</span> <br>
      email: cloudjaehun@gmail.com
      phone: +82-10-6689-5928
content:
  # Automatically link email and phone or display as text?
  autolink: true

  # Email form provider
  form:
    provider: netlify
    formspree:
      id:
    netlify:
      # Enable CAPTCHA challenge to reduce spam?
      captcha: false

design:
  columns: '1'
---
