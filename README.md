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

## Báo cáo tình hình kho ảnh (cập nhật 2026-11-25)

- **Tổng số ảnh (`manifest.json` & cây thư mục):** **5.137 ảnh** (~**1209,6 MB**) thuộc **12 nhóm** (tất cả `enabled: true`)
- **Tổng bản ghi `catalog.json`:** **4.773** (`review`: 4.729 · `customer_gallery`: 38 · `original`: 6 · `stock/listing/editorial`: **0**)
- **Kiểm tra trùng lặp:** **0 trùng MD5** toàn repo · **0 trùng SHA-256** toàn `catalog.json`

### Thống kê theo nhóm & danh mục

| Nhóm (`source_group`) | Số ảnh | Trong `catalog.json` | Dung lượng | Chi tiết danh mục (`category`) |
| --- | ---: | ---: | ---: | --- |
| **Nội thất** | **1.798** | 1,434 *(364 ảnh cũ chưa có catalog)* | 600,3 MB | `dining-tables` (195), `wall-neon` (161), `desks` (106), `coffee-tables` (99), `bookshelves` (96), `side-tables` (93), `chairs` (92), `media-consoles` (89), `sofas` (85), `sideboards` (84), `cabinets` (81), `beds` (68), `console-tables` (60), `dressers` (32), `floor-lamps` (28), `mirrors` (26), `table-lamps` (20), `rugs` (7), `ceiling-lights` (6), `ottomans` (6) |
| **Áo** | **1.535** | 1,535 | 343,5 MB | `tees-hoodies` (1351), `polo-shirts` (170), `team-jerseys` (14) |
| **Trang trí nhà cửa** | **784** | 784 | 139,6 MB | `ornaments` (254), `garden-flag` (215), `pillows` (163), `doormats` (79), `canvas` (32), `blankets` (18), `posters` (9), `memorial-stone` (6), `home-decor` (5), `acrylic-plaque` (3) |
| **Cốc và bình** | **670** | 670 | 74,2 MB | `drinkware` (670) |
| **Phụ kiện** | **143** | 143 | 18,8 MB | `keychains` (76), `jewelry` (66), `neckties` (1) |
| **Đồ thú cưng** | **75** | 75 | 11,4 MB | `pet-bowls` (47), `bandana` (19), `pet-food-mat` (9) |
| **Thể thao ngoài trời** | **37** | 37 | 6,7 MB | `outdoor-sports` (37) |
| **Mũ** | **27** | 27 | 3,7 MB | `hats` (27) |
| **Đồng phục** | **25** | 25 | 3,7 MB | `medical-scrubs` (25) |
| **Đồ lót** | **19** | 19 | 3,0 MB | `underwear` (19) |
| **Đồ bếp** | **13** | 13 | 2,7 MB | `oven-mitts` (13) |
| **Quần đùi** | **11** | 11 | 2,0 MB | `hawaiian-beachwear` (11) |
| **Tổng cộng** | **5.137** | **4.773** | **1209,6 MB** | |

### Nhật ký cập nhật (2026-11-25)

- **Đợt 1–3 (+1.457 ảnh review thật mới từ Judge.me):** toàn bộ đã kiểm trùng URL, `review_id`, MD5, SHA-256, perceptual hash (`16×16 dHash ≤ 20/256`) và duyệt trực quan từng contact sheet — loại bỏ sạch ảnh giả, studio, catalog nền trắng, screenshot, ảnh xoay ngang, hộp carton rỗng và góc chụp trùng.
  - Đợt 3 vừa bổ sung thêm **+601 ảnh** (tập trung mạnh vào các ngách nội thất gỗ mỏng như `sideboards`, `media-consoles` / tủ đĩa than, `console-tables` gỗ nguyên khối, `coffee-tables`, `dining-tables`, `bookshelves`, `mirrors`, `table-lamps`, `wall-neon`, cùng ảnh người thật mặc áo & khui hàng còn trong bì ở `Áo` và `Thể thao ngoài trời`).
- **Dọn dẹp & chuyển danh mục (-234 ảnh, chuyển 1 ảnh):**
  - Gỡ **52 ảnh stock/giả/catalog/editorial** (Pexels model trong `Áo` & `Thể thao ngoài trời`, listing/editorial trong `Nội thất`).
  - Gỡ **51 ảnh trùng MD5** và **3 ảnh trùng pHash** tồn đọng trong `Nội thất`.
  - Chuyển **1 ảnh chó đeo khăn bandana** từ `Áo` sang `Đồ thú cưng` (`f9549680-fdd3-423d-aa1c-bf7d2665a38c.jpg`).
  - Gỡ **12 ảnh chó thuần không có áo** + **17 ảnh không dùng được** trong `Áo`, **77 ảnh ngoài trời/cắm trại/xe/sân vườn** + **20 ảnh hộp/hỏng/tối** trong `Nội thất`, **4 ảnh ghép/mờ** trong `Đồng phục`, **1 ảnh dính banner** trong `Thể thao ngoài trời`.
