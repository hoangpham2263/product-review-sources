# Product Review Sources

Source images for Product Review, copied from the `Tools Hub/Product Review/Nguồn ảnh/` folder on Google Drive.

```text
source-photos/
├── catalog.json     image catalog used by the app
├── manifest.json    groups and files, with size, MD5 and enabled state
└── <group>/<image>  one folder per group, named as on Drive
```

Images are named `<uuid>.<ext>` in lowercase. The UUID is a random version 4 UUID. Extensions are `.jpg` or `.png`. The original file name and MD5 are kept as `originalName` and `md5` in `manifest.json`.

Image link:

```text
https://raw.githubusercontent.com/hoangpham2263/product-review-sources/main/source-photos/<group>/<uuid>.<ext>
```

Group names contain Vietnamese characters, so URL-encode them in requests.

## Báo cáo tình hình kho ảnh (cập nhật 2026-11-26)

- **Tổng số ảnh (`manifest.json` & cây thư mục):** **5.520 ảnh** (~**1423,1 MB**) thuộc **12 nhóm** (tất cả `enabled: true`)
- **Tổng bản ghi `catalog.json`:** **5.156** (`review`: 5.112 · `customer_gallery`: 38 · `original`: 6 · `stock/listing/editorial`: **0**)
- **Kiểm tra trùng lặp:** **0 trùng MD5** toàn repo · **0 trùng SHA-256** toàn `catalog.json`

### Thống kê theo nhóm & danh mục

| Nhóm (`source_group`) | Số ảnh | Trong `catalog.json` | Dung lượng | Chi tiết danh mục (`category`) |
| --- | ---: | ---: | ---: | --- |
| **Nội thất** | **2.302** | 1,938 *(364 ảnh cũ chưa có catalog)* | 770,6 MB | `dining-tables` (226), `wall-neon` (179), `side-tables` (148), `chairs` (140), `coffee-tables` (119), `desks` (113), `bookshelves` (113), `sofas` (104), `media-consoles` (98), `cabinets` (94), `sideboards` (89), `console-tables` (80), `beds` (70), `dressers` (65), `floor-lamps` (63), `table-lamps` (60), `mirrors` (59), `rugs` (59), `ottomans` (33), `ceiling-lights` (26) |
| **Áo** | **1.408** | 1,408 | 384,6 MB | `tees-hoodies` (1167), `polo-shirts` (229), `team-jerseys` (12) |
| **Trang trí nhà cửa** | **784** | 784 | 139,6 MB | `ornaments` (254), `garden-flag` (215), `pillows` (163), `doormats` (79), `canvas` (32), `blankets` (18), `posters` (9), `memorial-stone` (6), `home-decor` (5), `acrylic-plaque` (3) |
| **Cốc và bình** | **670** | 670 | 74,2 MB | `drinkware` (670) |
| **Phụ kiện** | **143** | 143 | 18,8 MB | `keychains` (76), `jewelry` (66), `neckties` (1) |
| **Đồ thú cưng** | **75** | 75 | 11,4 MB | `pet-bowls` (47), `bandana` (19), `pet-food-mat` (9) |
| **Thể thao ngoài trời** | **46** | 46 | 9,3 MB | `outdoor-sports` (46) |
| **Mũ** | **27** | 27 | 3,7 MB | `hats` (27) |
| **Đồng phục** | **22** | 22 | 3,3 MB | `medical-scrubs` (22) |
| **Đồ lót** | **19** | 19 | 3,0 MB | `underwear` (19) |
| **Đồ bếp** | **13** | 13 | 2,7 MB | `oven-mitts` (13) |
| **Quần đùi** | **11** | 11 | 2,0 MB | `hawaiian-beachwear` (11) |
| **Tổng cộng** | **5.520** | **5.156** | **1423,1 MB** | |

### Nhật ký cập nhật

- **Đợt 4 + 4B (2026-11-26 · +727 ảnh mới, dọn -344 ảnh lỗi cũ):**
  - Bổ sung **+727 ảnh review thật** từ các store Judge.me mới, lấp đầy các ngách mỏng trong `Nội thất` (`rugs`, `ceiling-lights`, `table-lamps`, `floor-lamps`, `dressers`, `ottomans`, `mirrors`, `console-tables`, `chairs`, `side-tables`, `wall-neon`) cùng `Áo` (`polo-shirts`, `tees-hoodies`, ảnh áo gấp/treo/khui gói) và `Thể thao ngoài trời`.
  - Soi toàn bộ 1.597 ảnh cũ ở `Áo`, `Thể thao ngoài trời`, `Đồng phục` và gỡ sạch **-344 ảnh lỗi** (ảnh thú cưng thuần không có áo, mockup nền trắng, ảnh chụp màn hình điện thoại/web, cốc/gối/nhầm đồ, ảnh xoay ngang 90°, ảnh ghép collage).
- **Đợt 1–3 (2026-11-25 · +1.457 ảnh review thật mới, dọn -234 ảnh, chuyển 1 ảnh):**
  - Toàn bộ đã kiểm trùng URL, `review_id`, MD5, SHA-256, perceptual hash (`16×16 dHash ≤ 20/256`) và duyệt trực quan từng contact sheet — loại sạch 52 ảnh stock/editorial Pexels, 54 ảnh trùng MD5/pHash cũ, ảnh hộp rỗng/ngoài trời/hỏng và chuyển 1 ảnh thú cưng sang `Đồ thú cưng`.
