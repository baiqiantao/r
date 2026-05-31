# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 概述

基于 GitHub 的博客图床仓库，仅包含静态图片文件，无代码、构建系统或测试。

## 目录结构

- `img/` — 所有图片，按年份分子目录存放（如 `img/2020/`、`img/2022/` 等）
- 图片命名规范：`YYYYMMDD_HHMMSS_N.ext`（时间戳 + 批次序号）
- 提交信息规范：`upload image: <文件名>`

## 分支

- `master` — 主分支
- `main` — 次分支

## 操作说明

上传图片：将文件放入对应的 `img/<年份>/` 目录，使用标准提交信息格式提交并推送。
