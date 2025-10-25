---
# A section created with the Portfolio widget.
# This section displays content from `content/project/`.
# See https://docs.hugoblox.com/widget/portfolio/
widget: portfolio

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 35

title: 프로젝트
subtitle: 학교 프로젝트 & 개인 프로젝트

content:
  # Page type to display. E.g. project.
  page_type: project

  # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
  filter_default: 0

  # Filter toolbar (optional).
  # Add or remove as many filters (`filter_button` instances) as you like.
  # To show all items, set `tag` to "*".
  # To filter by a specific tag, set `tag` to an existing tag name.
  # To remove the toolbar, delete the entire `filter_button` block.
  filter_button:
    - name: 모두
      tag: '*'
    - name: "'R'을 이용한 데이터 분석 프로젝트"
      tag: DA
    - name: "'C'를 이용한 자료구조"
      tag: DS
    - name: "'SQL'을 이용한 데이터베이스 프로젝트"
      tag: DB

design:
  columns: '1'
  view: masonry
  flip_alt_rows: true
  background: {}
  spacing: {padding: [0, 0, 0, 0]}
---
