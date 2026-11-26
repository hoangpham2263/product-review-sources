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

- **Tổng số ảnh (`manifest.json` & cây thư mục):** **16.492 ảnh** (~**5682,2 MB**) thuộc **20 nhóm** (tất cả `enabled: true`, **20/20 nhóm đều ≥ 500 ảnh**, thấp nhất **503 ảnh**)
- **Tổng bản ghi `catalog.json`:** **16.128** (`review`: 16.084 · `customer_gallery`: 38 · `original`: 6 · `stock/listing/editorial`: **0**)
- **Kiểm tra trùng lặp:** **0 trùng MD5** toàn repo · **0 trùng SHA-256** toàn `catalog.json`

### Thống kê theo nhóm & danh mục

| Nhóm (`source_group`) | Số ảnh | Trong `catalog.json` | Dung lượng | Chi tiết danh mục (`category`) |
| --- | ---: | ---: | ---: | --- |
| **Nội thất** | **3.313** | 2,949 *(364 ảnh cũ chưa có catalog)* | 1074,1 MB | `dining-tables` (327), `wall-neon` (284), `chairs` (261), `bookshelves` (207), `table-lamps` (200), `side-tables` (169), `rugs` (160), `coffee-tables` (136), `desks` (135), `cabinets` (129), `sofas` (125), `sideboards` (117), `media-consoles` (115), `floor-lamps` (111), `mirrors` (89), `beds` (87), `ceiling-lights` (87), `console-tables` (83), `dressers` (67), `ottomans` (60) |
| **Áo** | **2.148** | 2,148 | 685,3 MB | `tees-hoodies` (1682), `polo-shirts` (259), `team-jerseys` (207) |
| **Trang trí nhà cửa** | **1.334** | 1,334 | 361,8 MB | `ornaments` (254), `pillows` (241), `garden-flag` (215), `canvas` (194), `blankets` (175), `home-decor` (143), `doormats` (94), `posters` (9), `memorial-stone` (6), `acrylic-plaque` (3) |
| **Cốc và bình** | **988** | 988 | 185,0 MB | `drinkware` (988) |
| **Phụ kiện** | **703** | 703 | 248,9 MB | `jewelry` (315), `wallets-bags` (266), `keychains` (121), `neckties` (1) |
| **Mũ** | **584** | 584 | 238,6 MB | `hats` (584) |
| **Quần đùi** | **582** | 582 | 251,2 MB | `casual-shorts` (567), `hawaiian-beachwear` (15) |
| **Giày dép** | **567** | 567 | 220,0 MB | `boots` (235), `sneakers` (233), `slippers` (51), `sandals-slides` (48) |
| **Phụ kiện ô tô và xe máy** | **566** | 566 | 232,4 MB | `car-accessories` (227), `car-mats-covers` (198), `motorcycle-gear` (141) |
| **Mẹ và bé - Đồ chơi** | **533** | 533 | 237,5 MB | `baby-gear` (286), `toys-plushies` (247) |
| **Làm đẹp và chăm sóc cá nhân** | **532** | 532 | 167,5 MB | `fragrance-perfume` (207), `makeup-brushes` (168), `skincare-serums` (106), `hair-tools` (51) |
| **Đồ bếp** | **529** | 529 | 216,3 MB | `kitchen-tools` (252), `cookware` (113), `cutting-boards` (110), `aprons` (41), `oven-mitts` (13) |
| **Đồng phục** | **526** | 526 | 172,6 MB | `medical-scrubs` (526) |
| **Văn phòng phẩm và học tập** | **522** | 522 | 205,6 MB | `notebooks-planners` (311), `pens-stationery` (170), `desk-organizers-mats` (41) |
| **Đồ lót** | **521** | 521 | 175,0 MB | `underwear` (521) |
| **Thể thao ngoài trời** | **518** | 518 | 221,9 MB | `outdoor-sports` (518) |
| **Đồ công nghệ và điện tử** | **510** | 510 | 163,0 MB | `keyboards-desk-tech` (187), `headphones-audio` (183), `gadgets-chargers` (74), `phone-watch-accessories` (66) |
| **Quần dài và váy** | **510** | 510 | 157,2 MB | `dresses-skirts` (216), `pants-jeans` (185), `leggings-joggers` (109) |
| **Đồ thú cưng** | **503** | 503 | 192,5 MB | `pet-collars-harnesses` (269), `pet-beds` (122), `pet-bowls` (84), `bandana` (19), `pet-food-mat` (9) |
| **Sân vườn và ngoài trời** | **503** | 503 | 275,7 MB | `garden-planters` (257), `patio-furniture` (161), `solar-lights-decor` (85) |
| **Tổng cộng** | **16.492** | **16.128** | **5682,2 MB** | |

### Nhật ký cập nhật

- **Đợt 12C–F (2026-11-26 · +224 ảnh mới — hoàn tất 20/20 nhóm ≥ 500 ảnh):**
  - Chốt vượt mốc 500+ cho 2 nhóm cuối: `Đồ lót` (+169, 100% ảnh đặt phẳng/nguyên hộp sạch) và `Làm đẹp và chăm sóc cá nhân` (+55).
- **Đợt 12 + 12B (2026-11-26 · +1.092 ảnh mới — đẩy 8 nhóm vượt 500+):**
  - Đẩy vượt 500+ thêm 8 nhóm: `Quần đùi` (+235), `Phụ kiện ô tô và xe máy` (+165), `Sân vườn và ngoài trời` (+141), `Đồng phục` (+128), `Mẹ và bé - Đồ chơi` (+88), `Đồ bếp` (+64), `Văn phòng phẩm và học tập` (+36), `Quần dài và váy` (+22), cùng `Đồ lót` (+179) và `Làm đẹp` (+34).
- **Đợt 11 + 11B (2026-11-26 · +2.140 ảnh mới — hoàn thiện đủ 20 nhóm lớn & vượt mốc 15.000+ ảnh):**
  - Mở mới 4 nhóm cuối: `Văn phòng phẩm và học tập` (+486), `Mẹ và bé - Đồ chơi` (+445), `Phụ kiện ô tô và xe máy` (+401), `Sân vườn và ngoài trời` (+362), bồi thêm `Giày dép` (+125), `Đồ công nghệ` (+117), `Quần dài và váy` (+102), `Làm đẹp` (+66), `Đồ lót` (+36).
- **Đợt 10 (2026-11-26 · +1.395 ảnh mới):** Mở mới `Giày dép` (+442), `Đồ công nghệ và điện tử` (+393), `Quần dài và váy` (+386), bồi `Làm đẹp` (+174).
- **Đợt 9 + 9B (2026-11-26 · +1.394 ảnh mới):** Bơm đầy các mục mỏng & mở mới `Làm đẹp và chăm sóc cá nhân`.
- **Đợt 1–8 (2026-11-25 – 2026-11-26):** Xây nền 10.247 ảnh sạch trên 12 nhóm ban đầu, 0 trùng MD5/SHA-256/pHash.
