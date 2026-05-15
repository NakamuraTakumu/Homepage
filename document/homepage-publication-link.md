# Homepage Publication PDF Link

- Created: 2026-05-15 09:26 UTC
- Updated: 2026-05-15 09:26 UTC
- Model: gpt-5.5
- Reasoning-Effort: high
- Session: 019e2af1-dd3e-7f41-8498-4ef0d0e9427d
- Repository: /home/nakamura/homepage
- Related-Commit: none

Responsibility: Homepage の Publications に追加した `Functorial Gradient-Based Learning` の PDF 配置と検証結果を記録する。

## Background

Homepage に learnerParaLens の論文を追加した。

## Result

- `index.html` の Publications には論文タイトル、著者、`Manuscript, 2026`、PDF リンクを置いた。
- README にあった GitLab artifact URL は `curl -I -L --max-time 15` で `404` だったため、公開ページのリンク先には使わない。
- PDF は `papers/learnerParaLens.pdf` としてリポジトリに同梱し、Homepage から相対リンクで参照する。
- 静的サーバー `python3 -m http.server 8765` で `index.html` 内の追加項目と PDF の `200 OK` を確認した。

## Detail

- PDF の内容確認は `/home/nakamura/nakamura-24-master/document/learnerParaLens/learnerParaLens.pdf` の `pdftotext` 抽出で行った。
- DOI と受理日は manuscript 側に placeholder が残っていたため、Homepage には DOI や掲載決定情報を書かない。

## References

なし
