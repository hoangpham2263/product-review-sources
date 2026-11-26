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

- **Tổng số ảnh (`manifest.json` & cây thư mục):** **15.176 ảnh** (~**5163,2 MB**) thuộc **20 nhóm** (tất cả `enabled: true`)
- **Tổng bản ghi `catalog.json`:** **14.812** (`review`: 14.768 · `customer_gallery`: 38 · `original`: 6 · `stock/listing/editorial`: **0**)
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
| **Giày dép** | **567** | 567 | 220,0 MB | `boots` (235), `sneakers` (233), `slippers` (51), `sandals-slides` (48) |
| **Thể thao ngoài trời** | **518** | 518 | 221,9 MB | `outdoor-sports` (518) |
| **Đồ công nghệ và điện tử** | **510** | 510 | 163,0 MB | `keyboards-desk-tech` (187), `headphones-audio` (183), `gadgets-chargers` (74), `phone-watch-accessories` (66) |
| **Đồ thú cưng** | **503** | 503 | 192,5 MB | `pet-collars-harnesses` (269), `pet-beds` (122), `pet-bowls` (84), `bandana` (19), `pet-food-mat` (9) |
| **Quần dài và váy** | **488** | 488 | 148,5 MB | `dresses-skirts` (194), `pants-jeans` (185), `leggings-joggers` (109) |
| **Văn phòng phẩm và học tập** | **486** | 486 | 193,0 MB | `notebooks-planners` (275), `pens-stationery` (170), `desk-organizers-mats` (41) |
| **Đồ bếp** | **465** | 465 | 193,8 MB | `kitchen-tools` (237), `cookware` (94), `cutting-boards` (80), `aprons` (41), `oven-mitts` (13) |
| **Mẹ và bé - Đồ chơi** | **445** | 445 | 201,5 MB | `baby-gear` (239), `toys-plushies` (206) |
| **Làm đẹp và chăm sóc cá nhân** | **443** | 443 | 141,3 MB | `fragrance-perfume` (196), `makeup-brushes` (137), `skincare-serums` (59), `hair-tools` (51) |
| **Phụ kiện ô tô và xe máy** | **401** | 401 | 158,6 MB | `car-accessories` (163), `car-mats-covers` (128), `motorcycle-gear` (110) |
| **Đồng phục** | **398** | 398 | 137,5 MB | `medical-scrubs` (398) |
| **Sân vườn và ngoài trời** | **362** | 362 | 196,6 MB | `garden-planters` (177), `patio-furniture` (112), `solar-lights-decor` (73) |
| **Quần đùi** | **347** | 347 | 152,8 MB | `casual-shorts` (332), `hawaiian-beachwear` (15) |
| **Đồ lót** | **173** | 173 | 48,4 MB | `underwear` (173) |
| **Tổng cộng** | **15.176** | **14.812** | **5163,2 MB** | |

### Nhật ký cập nhật

- **Đợt 11 + 11B (2026-11-26 · +2.140 ảnh mới — hoàn thiện đủ 20 nhóm lớn & vượt mốc 15.000+ ảnh):**
  - Mở mới 4 nhóm cuối: `Văn phòng phẩm và học tập` (+486), `Mẹ và bé - Đồ chơi` (+445), `Phụ kiện ô tô và xe máy` (+401), `Sân vườn và ngoài trời` (+362), đồng thời bồi thêm `Giày dép` (+125), `Đồ công nghệ và điện tử` (+117), `Quần dài và váy` (+102), `Làm đẹp và chăm sóc cá nhân` (+66), `Đồ lót` (+36).
- **Đợt 10 (2026-11-26 · +1.395 ảnh mới — mở thêm 3 nhóm lớn & bồi nhóm Làm đẹp):**
  - Mở mới `Giày dép` (+442), `Đồ công nghệ và điện tử` (+393), `Quần dài và váy` (+386), và bổ sung `Làm đẹp và chăm sóc cá nhân` (+174).
- **Đợt 9 + 9B (2026-11-26 · +1.394 ảnh mới — bơm đầy các mục mỏng & mở nhóm Làm đẹp):**
  - Bơm mạnh `Đồng phục` (+281), `Làm đẹp và chăm sóc cá nhân` (+203), `Áo :: team-jerseys` (+195), `Mũ` (+174), `Quần đùi` (+131), `Thể thao ngoài trời` (+131), `Đồ lót` (+114, 100% ảnh phẳng/hộp sạch), `Đồ bếp` (+95), `Trang trí nhà cửa` (+70).
- **Đợt 8 (2026-11-26 · +1.294 ảnh mới phủ rộng 10 nhóm — vượt mốc 10.000+ ảnh):**
  - Bổ sung mạnh `Phụ kiện` (+222), `Nội thất` (+195), `Áo` (+172), `Trang trí nhà cửa` (+121), `Mũ` (+112), `Cốc và bình` (+104), `Đồ thú cưng` (+101), `Thể thao ngoài trời` (+94), `Đồ bếp` (+92), `Quần đùi` (+81).
- **Đợt 7 (2026-11-26 · +1.396 ảnh mới phủ rộng 10 nhóm):**
  - Bổ sung mạnh `Trang trí nhà cửa` (+236), `Phụ kiện` (+223), `Đồ thú cưng` (+183), `Nội thất` (+169), `Cốc và bình` (+146), `Đồ bếp` (+115), `Áo` (+111), `Thể thao ngoài trời` (+105), `Mũ` (+82), `Quần đùi` (+26).
- **Đợt 6 (2026-11-26 · +944 ảnh mới phủ rộng 10 nhóm):**
  - Đẩy vượt mốc 100+ ảnh cho các nhóm từng mỏng nhất: `Đồng phục` (+95), `Quần đùi` (+82), `Mũ` (+89), `Thể thao ngoài trời` (+81), `Đồ thú cưng` (+100).
- **Đợt 5 + 5B (2026-11-26 · +1.093 ảnh mới phủ rộng 9 nhóm):**
  - Bổ sung mạnh `Nội thất` (+460), `Áo` (+183), `Phụ kiện` (+115), `Đồ bếp` (+110), `Mũ` (+100), `Thể thao ngoài trời` (+61), `Đồ thú cưng` (+44), `Quần đùi` (+16), `Đồ lót` (+4).
- **Đợt 4 + 4B (2026-11-26 · +727 ảnh mới, dọn -344 ảnh lỗi cũ):**
  - Bổ sung ngách `Nội thất` & `Áo :: polo-shirts`, và soi sạch toàn bộ 1.597 ảnh cũ ở `Áo`, `Thể thao ngoài trời`, `Đồng phục` để gỡ 344 ảnh lỗi.
- **Đợt 1–3 (2026-11-25 · +1.457 ảnh mới, dọn -234 ảnh, chuyển 1 ảnh):**
  - Kiểm trùng 4 lớp (URL, `review_id`, MD5/SHA-256, pHash) và duyệt trực quan contact sheet, loại sạch 52 ảnh stock/editorial Pexels và 54 ảnh trùng cũ.
