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

- **Tổng số ảnh (`manifest.json` & cây thư mục):** **7.557 ảnh** (~**2155,8 MB**) thuộc **12 nhóm** (tất cả `enabled: true`)
- **Tổng bản ghi `catalog.json`:** **7.193** (`review`: 7.149 · `customer_gallery`: 38 · `original`: 6 · `stock/listing/editorial`: **0**)
- **Kiểm tra trùng lặp:** **0 trùng MD5** toàn repo · **0 trùng SHA-256** toàn `catalog.json`

### Thống kê theo nhóm & danh mục

| Nhóm (`source_group`) | Số ảnh | Trong `catalog.json` | Dung lượng | Chi tiết danh mục (`category`) |
| --- | ---: | ---: | ---: | --- |
| **Nội thất** | **2.949** | 2,585 *(364 ảnh cũ chưa có catalog)* | 951,2 MB | `dining-tables` (284), `wall-neon` (284), `chairs` (199), `side-tables` (159), `bookshelves` (152), `coffee-tables` (136), `desks` (135), `cabinets` (129), `sofas` (125), `table-lamps` (122), `media-consoles` (115), `floor-lamps` (111), `sideboards` (99), `beds` (87), `ceiling-lights` (87), `rugs` (85), `console-tables` (83), `dressers` (67), `mirrors` (66), `ottomans` (60) |
| **Áo** | **1.670** | 1,670 | 473,3 MB | `tees-hoodies` (1400), `polo-shirts` (258), `team-jerseys` (12) |
| **Trang trí nhà cửa** | **907** | 907 | 188,2 MB | `ornaments` (254), `garden-flag` (215), `pillows` (166), `canvas` (109), `doormats` (79), `blankets` (54), `home-decor` (12), `posters` (9), `memorial-stone` (6), `acrylic-plaque` (3) |
| **Cốc và bình** | **738** | 738 | 94,1 MB | `drinkware` (738) |
| **Phụ kiện** | **258** | 258 | 65,5 MB | `keychains` (117), `jewelry` (94), `wallets-bags` (46), `neckties` (1) |
| **Đồ thú cưng** | **219** | 219 | 75,9 MB | `pet-collars-harnesses` (88), `pet-beds` (54), `pet-bowls` (49), `bandana` (19), `pet-food-mat` (9) |
| **Mũ** | **216** | 216 | 89,3 MB | `hats` (216) |
| **Thể thao ngoài trời** | **188** | 188 | 73,2 MB | `outdoor-sports` (188) |
| **Đồ bếp** | **163** | 163 | 65,0 MB | `cutting-boards` (76), `cookware` (41), `kitchen-tools` (22), `oven-mitts` (13), `aprons` (11) |
| **Đồng phục** | **117** | 117 | 38,2 MB | `medical-scrubs` (117) |
| **Quần đùi** | **109** | 109 | 38,0 MB | `casual-shorts` (94), `hawaiian-beachwear` (15) |
| **Đồ lót** | **23** | 23 | 3,9 MB | `underwear` (23) |
| **Tổng cộng** | **7.557** | **7.193** | **2155,8 MB** | |

### Nhật ký cập nhật

- **Đợt 6 (2026-11-26 · +944 ảnh mới phủ rộng 10 nhóm):**
  - Đẩy vượt mốc 100+ ảnh cho các nhóm từng mỏng nhất: `Đồng phục` (+95), `Quần đùi` (+82), `Mũ` (+89), `Thể thao ngoài trời` (+81), `Đồ thú cưng` (+100), cùng `Nội thất` (+187), `Trang trí nhà cửa` (+123), `Áo` (+79), `Cốc và bình` (+68), `Đồ bếp` (+40).
- **Đợt 5 + 5B (2026-11-26 · +1.093 ảnh mới phủ rộng 9 nhóm):**
  - Bổ sung mạnh `Nội thất` (+460), `Áo` (+183), `Phụ kiện` (+115), `Đồ bếp` (+110), `Mũ` (+100), `Thể thao ngoài trời` (+61), `Đồ thú cưng` (+44), `Quần đùi` (+16), `Đồ lót` (+4) kèm ưu tiên ảnh nguyên hộp/chưa khui.
- **Đợt 4 + 4B (2026-11-26 · +727 ảnh mới, dọn -344 ảnh lỗi cũ):**
  - Bổ sung ngách `Nội thất` & `Áo :: polo-shirts`, và soi sạch toàn bộ 1.597 ảnh cũ ở `Áo`, `Thể thao ngoài trời`, `Đồng phục` để gỡ 344 ảnh lỗi.
- **Đợt 1–3 (2026-11-25 · +1.457 ảnh mới, dọn -234 ảnh, chuyển 1 ảnh):**
  - Kiểm trùng 4 lớp (URL, `review_id`, MD5/SHA-256, pHash) và duyệt trực quan contact sheet, loại sạch 52 ảnh stock/editorial Pexels và 54 ảnh trùng cũ.
