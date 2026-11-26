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

- **Tổng số ảnh (`manifest.json` & cây thư mục):** **6.613 ảnh** (~**1778,4 MB**) thuộc **12 nhóm** (tất cả `enabled: true`)
- **Tổng bản ghi `catalog.json`:** **6.249** (`review`: 6.205 · `customer_gallery`: 38 · `original`: 6 · `stock/listing/editorial`: **0**)
- **Kiểm tra trùng lặp:** **0 trùng MD5** toàn repo · **0 trùng SHA-256** toàn `catalog.json`

### Thống kê theo nhóm & danh mục

| Nhóm (`source_group`) | Số ảnh | Trong `catalog.json` | Dung lượng | Chi tiết danh mục (`category`) |
| --- | ---: | ---: | ---: | --- |
| **Nội thất** | **2.762** | 2,398 *(364 ảnh cũ chưa có catalog)* | 893,4 MB | `wall-neon` (275), `dining-tables` (268), `chairs` (185), `side-tables` (153), `desks` (130), `coffee-tables` (126), `sofas` (118), `bookshelves` (113), `floor-lamps` (110), `table-lamps` (110), `media-consoles` (108), `cabinets` (97), `sideboards` (91), `ceiling-lights` (86), `rugs` (84), `console-tables` (80), `beds` (78), `dressers` (66), `mirrors` (61), `ottomans` (59) |
| **Áo** | **1.591** | 1,591 | 437,4 MB | `tees-hoodies` (1330), `polo-shirts` (249), `team-jerseys` (12) |
| **Trang trí nhà cửa** | **784** | 784 | 139,6 MB | `ornaments` (254), `garden-flag` (215), `pillows` (163), `doormats` (79), `canvas` (32), `blankets` (18), `posters` (9), `memorial-stone` (6), `home-decor` (5), `acrylic-plaque` (3) |
| **Cốc và bình** | **670** | 670 | 74,2 MB | `drinkware` (670) |
| **Phụ kiện** | **258** | 258 | 65,5 MB | `keychains` (117), `jewelry` (94), `wallets-bags` (46), `neckties` (1) |
| **Mũ** | **127** | 127 | 49,4 MB | `hats` (127) |
| **Đồ bếp** | **123** | 123 | 41,0 MB | `cutting-boards` (47), `cookware` (41), `kitchen-tools` (22), `oven-mitts` (13) |
| **Đồ thú cưng** | **119** | 119 | 33,3 MB | `pet-bowls` (48), `pet-collars-harnesses` (43), `bandana` (19), `pet-food-mat` (9) |
| **Thể thao ngoài trời** | **107** | 107 | 29,2 MB | `outdoor-sports` (107) |
| **Quần đùi** | **27** | 27 | 8,2 MB | `casual-shorts` (16), `hawaiian-beachwear` (11) |
| **Đồ lót** | **23** | 23 | 3,9 MB | `underwear` (23) |
| **Đồng phục** | **22** | 22 | 3,3 MB | `medical-scrubs` (22) |
| **Tổng cộng** | **6.613** | **6.249** | **1778,4 MB** | |

### Nhật ký cập nhật

- **Đợt 5 + 5B (2026-11-26 · +1.093 ảnh mới phủ rộng 10 nhóm lớn):**
  - Mở rộng đồng loạt các danh mục còn mỏng kèm ưu tiên ảnh chụp **nguyên hộp / còn bọc nilon / mới nhận hàng**: `Nội thất` (+460, nổi bật `wall-neon`, `rugs`, `ceiling-lights`, `table-lamps`, `floor-lamps`, `ottomans`), `Áo` (+183), `Phụ kiện` (+115), `Đồ bếp` (+110), `Mũ` (+100), `Thể thao ngoài trời` (+61), `Đồ thú cưng` (+44), `Quần đùi` (+16), `Đồ lót` (+4).
- **Đợt 4 + 4B (2026-11-26 · +727 ảnh mới, dọn -344 ảnh lỗi cũ):**
  - Bổ sung mạnh các ngách `Nội thất` mỏng, `Áo :: polo-shirts` & `tees-hoodies`, và soi sạch toàn bộ 1.597 ảnh cũ ở `Áo`, `Thể thao ngoài trời`, `Đồng phục` để gỡ 344 ảnh thú cưng thuần/mockup/screenshot/nhầm đồ/xoay ngang.
- **Đợt 1–3 (2026-11-25 · +1.457 ảnh review thật mới, dọn -234 ảnh, chuyển 1 ảnh):**
  - Toàn bộ đã kiểm trùng URL, `review_id`, MD5, SHA-256, perceptual hash (`16×16 dHash ≤ 20/256`) và duyệt trực quan từng contact sheet — loại sạch 52 ảnh stock/editorial Pexels, 54 ảnh trùng MD5/pHash cũ và ảnh lỗi.
