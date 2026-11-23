# SUGAR WORKS · GitHub-managed portfolio

## Site
- Preview path: https://sheeny6-cmyk.github.io/magic-sugar-game/sugar-works/
- Source: `sugar-works/index.html`
- Existing ChatGPT Sites archive: https://sugar-works-gallery.sugar0506.chatgpt.site/
- Legacy administrator: https://sugar-works-gallery.sugar0506.chatgpt.site/admin

This is a **new front-end, not a complete export** of the ChatGPT Sites project. Original Works/Admin have NOT been deleted or changed.

## Completed (2026-11-22)
- Responsive ivory/lilac SUGAR WORKS creative landing page with ballet palace imagery
- Archive grid and functioning category filters for 6 portfolio project groups; OGQ lives in a dedicated collection section (non-owned snowboard entry removed)
- Direct links to ballet kingdom/cafe game
- Naver OGQ links: initial Sugar Ballet stickers https://naver.me/x52dbBni and **발레 쇼핑에 진심인 슈가** https://naver.me/GGGt2vH1 (saved earlier, live redirect not independently verified)
- YouTube, Instagram and Threads links
- Mobile layouts for small screens

## In-site Instatoon & Reels viewer (2026-11-22)
- New section `#toon` (`02 / INSTATOON & REELS`) between `#works` and `#ogq`. Nothing in it sends the visitor to Instagram to see a work: every image cut and every reel opens in an in-page modal viewer.
- **Image toons (4 series / 30 cuts)**, stored under `sugar-works/assets/toons/`:
  - `allegro/` 01–08 「미들 알레그로가 끝나지 않아!」 — downloaded from `sugar-works-gallery…/works/middle-allegro` (`/api/media/allegro-0N`), 810×1440 webp.
  - `kingdom/` 01–05 「발레왕국의 2027년 준비」 — same gallery (`/api/media/kingdom-0N`), 810×1440 webp.
  - `ending/` 01–09 「취발러의 엔딩은 죽음뿐」 — copied from `town/garden/assets/story/01–09.webp` (the garden prologue cuts), re-encoded to 810 px.
  - `misconception/` 01–08 「발레 16년 했어요」 — the Instagram carousel post of 2026-07-20 (`/p/DbCJVF9Er15/`), 810 px webp.
- **Reels (12 videos, 22 MB total)**, stored under `sugar-works/assets/reels/` as `NN-<shortcode>.mp4` + `NN-<shortcode>.webp` poster.
  - All 12 reels currently on the public profile `instagram.com/sugar.ballet/reels/` were extracted **from the profile's own media JSON (`video_versions` type 101, progressive 720×1280 with AAC audio)** and re-encoded to H.264 CRF 28 + `+faststart` for the repository (37 MB → 22 MB). No reel fell back to a poster-only card and none needed a YouTube substitute.
  - Source pages are recorded per item in `REELS` inside `index.html` (`https://www.instagram.com/sugar.ballet/reel/<shortcode>/`). Instagram's `/reel/<code>/embed/` endpoint is broken for this profile (“링크가 잘못되었거나…”) and is deliberately **not** used.
  - Reel titles are the on-frame headline when the video has one, otherwise the author's own caption. No invented titles.
- Viewer behaviour: arrow buttons, keyboard ←/→, swipe, cut counter, thumbnail strip, `세로 보기` (continuous scroll for image series), per-series switcher, and a link to the original post. Escape/backdrop/✕ closes; focus and body scroll are restored.
- The `인스타툰` filter in `01 / CREATIVE ARCHIVE` no longer bounces to the legacy gallery: it filters the grid and opens the viewer, and the `발레 인스타툰` card is a viewer button (`▷`).

## Calendar cards now open the in-site viewer (2026-11-22)
- `01 / CREATIVE ARCHIVE`의 두 달력 카드가 더 이상 기존 갤러리(`ORIGINAL`)로 나가지 않고, 사이트 내 뷰어에서 바로 열립니다.
  - 「발레왕국 달력 소개」 → `kingdom` 시리즈 「발레왕국의 2027년 준비」 5컷.
  - 「발레왕국 달력」 → `calendar` 시리즈 「2027 슈가공주 달력」 12장(1월~12월 넘겨 보기 / 세로로 이어 보기 / 썸네일 스트립).
- 12장 이미지는 `sugar-works-gallery…/works/calendar-2027`의 `/api/media/calendar-01`~`calendar-12`에서 받아 `sugar-works/assets/toons/calendar/01.webp`~`12.webp`로 저장했습니다. 원본 665×1440(세로 배경화면)을 810px 이하로 유지하며 webp q82로 재인코딩(합계 약 1.9MB).
- `calendar` 시리즈는 `noCard:true`라서 인스타툰 그리드에는 카드가 생기지 않습니다(그리드 집계 4 시리즈/30컷 유지). 뷰어의 시리즈 전환 줄에는 함께 나옵니다.
- 두 카드는 시리즈 첫 컷을 커버 이미지로 쓰고 `▷` 표시와 `▷ 2027 달력 12장 보기` / `▷ 5컷 달력 소개 보기` 문구를 답니다.
- 뷰어 API에 `window.SugarToons.openId(id, cut)`를 추가해 카드에서 특정 시리즈를 바로 열 수 있게 했습니다.

## Important content safety rules
- Show **only real, actually published projects**. Never invent work, testimonials, thumbnails or personal experiences.
- The six portfolio cards are project-category labels and *typographic category covers*, not the original artwork files. Only the ballet cafe uses an existing game asset.
- For any card without a confirmed deep link, link back to the original legacy gallery.
- Do not expose private drafts or internal data.
- Never pretend original Sites login/upload/edit/delete features are migrated. They remain in the old system.

## To complete the migration
1. Secure the original Sites project source or individual work records, media and per-project URLs.
2. Replace typographic covers and generic titles with verified original titles/preview media.
3. Move the site to its own GitHub repository/domain. This initial version is intentionally inside a separate folder of the existing game repository so game source files are untouched.
4. If an administrator is required on the new site, implement actual authentication, private storage, publishing states, and a secure data store. Static GitHub Pages alone does not provide secure Admin.
5. Add the ballet-note application only when its public, functioning URL has been verified.

## Editing from a normal ChatGPT chat
Update only `sheeny6-cmyk/magic-sugar-game/sugar-works/`. Report the exact commit, and distinguish source updates from deployment verification. Do not edit the sibling game directories.

## OGQ collection update (2026-11-22)
- The OGQ works are not limited to 2: a dedicated section exists at `/sugar-works/#ogq`.
- Confirmed direct-link entries from prior context: SET 01 https://naver.me/x52dbBni; SET 02 https://naver.me/GGGt2vH1. Current redirect destinations were not independently accessible.
- 「슈가공주의 일상」 passed review on Nov 16, 2026, per the user's Google Drive OGQ master plan, but its live sales link is not yet verified, so no invented link/status.
- 「발레리노 루카의 척척 리액션」 has 24-piece source/planning materials, but no publication confirmation; do not list as for sale.
- The user supplied their OGQ creator URL: https://naver.me/5Z1FxGzR . The portfolio now links there prominently for the complete catalog.
- The shortlink did not resolve to a readable creator/product listing through available external reading tools. Do not claim all individual stickers have been indexed until their titles and sales URLs are retrievable and verified.

## 6-tab structure · YouTube shorts · WRITING (2026-11-23)
- The top tab bar is now `WORKS · TOON & VIDEO · WRITING · NAVER OGQ · ABOUT · SUGAR WORLD` (`SUGAR WORLD` stays last). `#youtube`, `#instatoon` and `#reels` are aliases that open the `toon` panel (`canon()` in the tab script). Panel order in the DOM is works/toon/writing/ogq/world/about.
- **TOON & VIDEO (`#toon`)** keeps the existing 16-post Insta feed (4 toons / 30 cuts + 12 reels) and adds:
  - a chip row linking `@sugar.ballet` on Instagram, YouTube and Threads;
  - a filter group `전체 24 · 인스타툰·릴스 16 · 유튜브 숏츠 8` that toggles the two `.tv-set` blocks (`.tv-set[hidden]`);
  - a YouTube block: the channel's own banner + avatar (`assets/yt/channel-banner.webp`, `channel-avatar.webp`, taken from the public channel page) and **all 8 shorts** currently on `youtube.com/@sugar.ballet` (channel has no long-form videos tab). Titles/dates are the channel's own (`2026.10.30`–`2026.11.18`); no duration is shown because YouTube denied unauthenticated player extraction (`Sign in to confirm you're not a bot`).
  - Thumbnails are stored locally as `assets/yt/NN-<videoId>.webp` (480 px wide, from YouTube's `oar2.jpg` 720×1280 vertical frame; `joCplQz0_3o` only exists at 406×722). Each card opens `https://www.youtube.com/shorts/<id>` in a new tab — an in-page embed was deliberately not added because embeddability could not be verified from here and YouTube's own player/app is the reliable path.
- **WRITING (`#writing`, new)**: lilac magazine-style card grid — 01 「미치도록 아름다운 크리스마스」 (feature card, `brunch.co.kr/brunchbook/crazybchristmas`, 매주 화요일 · 1~20화), 02 브런치 `@sheeny6` (필명 루네), 03 티스토리 에튀튀드, 04 네이버 블로그 티나는 여행 중 (`sugaramor0506`), 05 네이버 블로그 슈가의 우당탕탕 일상 (`sugaramor`). Brunch pages redirect to a sign-in wall for anonymous readers, so episode counts come from the user's own copy and were not re-verified here.
- **NAVER OGQ (`#ogq`)** gains a goods card under the three sticker sets: 2027 슈가공주 달력 12장 — cover + 3 month previews, a `▷ 사이트에서 12장 보기` button that opens the existing in-site `calendar` viewer (`data-open-calendar` → `SugarToons`), and a link to the Tistory post for the wallpaper download.
- Kickers renumbered: 01 WORKS, 02 TOON & VIDEO, 03 WRITING & SERIALS, 04 ORIGINAL STICKER SERIES, 05 ABOUT THE CREATOR, 06 THE UNIVERSE. `town/` was not touched in this change.

## Ballet Note card · About poster (2026-11-23)
- **About (`#about`)**: the `S✳W` monogram (`.about-art` with the ✳ glyph) is gone. The left column is now a rounded poster frame — `assets/hero-kingdom-spirits.webp` in a 1122/1402 frame with an inner hairline and a small `SUGAR WORKS. / BALLET · STORY · ILLUSTRATION` caption badge. The About copy now lists 앱 alongside 발레·글쓰기·그림·영상 and names 발레노트.
- **WORKS (`#works`)**: new card 01 「발레노트 (Ballet Note)」 (`type:"app"`, filter category `게임·웹`). It is the first card built as an `<article>` with two links (`links:[…]`) instead of one `href`, so the renderer now appends `.card-actions` with **Google Play ↗** and **웹앱 열기 ↗**. Cover is the Tistory post's own 800×450 key image; the app's Play icon rides in a `.cover-icon` badge at the top-right. Archive count `05 → 06`.
- **SUGAR WORLD (`#world`)**: third tile `APP · 03` spanning both columns — app icon, copy and the same two links; on ≥900 px the 800×450 key image sits on the right as `.world-app-shot`.
- Links (both returned HTTP 200 and render on 2026-11-23):
  - Google Play `https://play.google.com/store/apps/details?id=com.sugar.balletnote` — page title 「발레노트 - Google Play 앱」, developer 슈가.
  - Web app `https://ballet-note-ten.vercel.app` — Next.js PWA, `<title>발레노트 Ballet Note</title>`, renders the home screen. `https://ballet-log.vercel.app` also answers 200 but is not used.
- Assets added: `assets/ballet-note.webp` (800×450, from the Tistory post's `img1.daumcdn.net` key image, q84) and `assets/ballet-note-icon.webp` (256×256 from the Play icon, q88). Both local; no hotlinked media.
- The `ballet-note` migration item above is now satisfied: the app is listed only with these two verified public URLs.
- `town/` was not touched. A local `town/garden/garden.js` modification was left unstaged and out of this commit.

## Games removed · Ballet Note only (2026-11-23)
- The user chose to drop the unfinished game projects from the portfolio and keep the 「발레노트」 app only. The top bar is now `WORKS · TOON & VIDEO · WRITING · NAVER OGQ · ABOUT` (5 tabs); the `SUGAR WORLD` tab and `#panel-world` were deleted, so an old `#world` link falls back to `works` through `fromHash()`.
- **WORKS**: the 「슈가의 마법 발레 카페」 card was deleted. The archive renders 5 cards numbered `01–05`, and both counts (`#workCount`, `#workCountAll`) read `05`. Card 01 「발레노트 (Ballet Note)」 keeps its `Google Play ↗` / `웹앱 열기 ↗` links and the `앱·웹` cover label.
- Filter chip `게임·웹` → `앱` (`data-filter="app"`); `types` now maps `app:"app"`. The renderer's `type:"game"` cafe-cover branch went with the card.
- Last game links out of `sugar-works/` removed: the two SUGAR WORLD tiles (`/cafe/`, `/town/`, plus the `../cafe`·`../town` image paths) and the `발레왕국 마을에서 보기 ↗` source link on the 「취발러의 엔딩은 죽음뿐」 toon (→ `town/garden/`). The toon, its cuts and its description stay.
- Copy: meta description and intro summary now read `영상과 앱` instead of `영상과 게임`. About copy already said 앱.
- The `.world*` CSS rules remain in the stylesheet but nothing in the markup uses them any more.
- `town/` was not touched. The local `town/garden/garden.js` modification was left unstaged and out of this commit.
- Checked at 390×844 (local, then live `?v=20261123c`): 5 tabs paint and switch, `#youtube` alias still opens `toon`, `#world` lands on `works`, filter chips show `앱/인스타툰/굿즈/영상`, no console errors, no HTTP ≥400, no broken images, no page-level horizontal overflow (only the tab bar scrolls sideways by design).

## Shorts collage card · YouTube-first TOON & VIDEO (2026-11-23)
- **WORKS 「발레툰 숏츠」 cover** now shows the channel's own shorts instead of one illustration. `assets/yt-shorts-collage.webp` (984×1224 webp q90, ~110 KB) is a 2×2 collage of the four newest YouTube thumbnails (`assets/yt/01-9JNZiiKifl0` · `02-UdcQLwwqPFA` · `03-QMmAzMASGSI` · `04-nCL3iaObt4g`), each cropped to 480×600 so the speech bubbles and faces stay in frame, on the site's lavender `#f6f0ff` with 24 px gutters. The cell ratio (0.804) matches the 390 px-card cover (169×210) so nothing is cropped on a phone; on the 3-column desktop grid the bottom row loses only its legs. `assets/video-thumb.webp` is no longer referenced (file kept).
- **Card click goes straight to the shorts**: the card is `url:"#youtube"`, so it pushes `#youtube` (not `#toon`) and lands on the TOON & VIDEO tab with the ① 유튜브 숏츠 section right under the sticky tab bar. Its aria-label reads `발레툰 숏츠 — 유튜브 숏츠 섹션 바로 보기` (`jump` field in the works array).
- **YouTube block moved first** in `#panel-toon` (`data-set="yt"` now carries `id="youtube"`), Insta feed second. Tally reads `24 PIECES / SHORTS 8 · INSTA 16`; the filter chips are `전체 24 · 유튜브 숏츠 8 · 인스타툰·릴스 16` in the same order as the blocks.
- **Routing**: the tab script keeps the raw hash (`rawHash()`) and passes it to `tvHook()` after every `go()`. `#youtube`/`#shorts` → `window.SugarTV.focusYt()` (activate the `yt` filter, then scroll `#youtube` to just below `#tabbar`), `#toon` → `window.SugarTV.set("all")` so the plain tab still opens the full 24. A direct `?…#youtube` load does the same from the TOON script's own `load` hook (30 ms after the tab script's scroll).
- Checked at 390×844 (local then live `?v=20261123d`) and 1280×900: card → `#youtube` + `yt` pressed + section at `top 57` under a 55 px tab bar; direct `#youtube` identical; `#toon` resets to 전체; block order yt→insta; no console errors, no page errors, no HTTP ≥400, no broken images, no horizontal overflow.
