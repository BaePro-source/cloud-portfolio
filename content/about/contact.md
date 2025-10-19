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
content:
  # Automatically link email and phone or display as text?
  email: cloudjaehun@gmail.com
  phone: 010-6689-5928
  address:
    stree: 삼송3길 11 갤럭시하우스 103호
    city: 전주시
    region: 전라북도
    country: 대한민국
    office_hours:
      - '연중무휴'
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
