language: python
python:
  - "3.5.3"
  - "3.6.1"
install:
  - pip install -r requirements.txt
script:
  - python -m compileall ./appuselfbot.py
  - python -m compileall ./cogs
  - python ./appuselfbot.py --test-run
cache: pip
notifications:
  email: false
dist: trusty
os: linux
