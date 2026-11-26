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

- **Tổng số ảnh (`manifest.json` & cây thư mục):** **8.953 ảnh** (~**2718,3 MB**) thuộc **12 nhóm** (tất cả `enabled: true`)
- **Tổng bản ghi `catalog.json`:** **8.589** (`review`: 8.545 · `customer_gallery`: 38 · `original`: 6 · `stock/listing/editorial`: **0**)
- **Kiểm tra trùng lặp:** **0 trùng MD5** toàn repo · **0 trùng SHA-256** toàn `catalog.json`

### Thống kê theo nhóm & danh mục

| Nhóm (`source_group`) | Số ảnh | Trong `catalog.json` | Dung lượng | Chi tiết danh mục (`category`) |
| --- | ---: | ---: | ---: | --- |
| **Nội thất** | **3.118** | 2,754 *(364 ảnh cũ chưa có catalog)* | 1010,5 MB | `dining-tables` (306), `wall-neon` (284), `chairs` (248), `bookshelves` (173), `side-tables` (169), `table-lamps` (150), `coffee-tables` (136), `desks` (135), `cabinets` (129), `sofas` (125), `rugs` (118), `media-consoles` (115), `floor-lamps` (111), `sideboards` (99), `beds` (87), `ceiling-lights` (87), `console-tables` (83), `mirrors` (72), `dressers` (67), `ottomans` (60) |
| **Áo** | **1.781** | 1,781 | 530,3 MB | `tees-hoodies` (1511), `polo-shirts` (258), `team-jerseys` (12) |
| **Trang trí nhà cửa** | **1.143** | 1,143 | 279,9 MB | `ornaments` (254), `garden-flag` (215), `canvas` (192), `pillows` (166), `blankets` (131), `home-decor` (88), `doormats` (79), `posters` (9), `memorial-stone` (6), `acrylic-plaque` (3) |
| **Cốc và bình** | **884** | 884 | 141,0 MB | `drinkware` (884) |
| **Phụ kiện** | **481** | 481 | 160,8 MB | `jewelry` (207), `wallets-bags` (156), `keychains` (117), `neckties` (1) |
| **Đồ thú cưng** | **402** | 402 | 159,0 MB | `pet-collars-harnesses` (170), `pet-beds` (120), `pet-bowls` (84), `bandana` (19), `pet-food-mat` (9) |
| **Mũ** | **298** | 298 | 119,6 MB | `hats` (298) |
| **Thể thao ngoài trời** | **293** | 293 | 126,2 MB | `outdoor-sports` (293) |
| **Đồ bếp** | **278** | 278 | 101,7 MB | `cookware` (94), `kitchen-tools` (84), `cutting-boards` (76), `oven-mitts` (13), `aprons` (11) |
| **Quần đùi** | **135** | 135 | 47,3 MB | `casual-shorts` (120), `hawaiian-beachwear` (15) |
| **Đồng phục** | **117** | 117 | 38,2 MB | `medical-scrubs` (117) |
| **Đồ lót** | **23** | 23 | 3,9 MB | `underwear` (23) |
| **Tổng cộng** | **8.953** | **8.589** | **2718,3 MB** | |

### Nhật ký cập nhật

- **Đợt 7 (2026-11-26 · +1.396 ảnh mới phủ rộng 10 nhóm):**
  - Bổ sung mạnh `Trang trí nhà cửa` (+236), `Phụ kiện` (+223), `Đồ thú cưng` (+183), `Nội thất` (+169), `Cốc và bình` (+146), `Đồ bếp` (+115), `Áo` (+111), `Thể thao ngoài trời` (+105), `Mũ` (+82), `Quần đùi` (+26) ưu tiên ảnh nhận hàng/chưa khui.
- **Đợt 6 (2026-11-26 · +944 ảnh mới phủ rộng 10 nhóm):**
  - Đẩy vượt mốc 100+ ảnh cho các nhóm từng mỏng nhất: `Đồng phục` (+95), `Quần đùi` (+82), `Mũ` (+89), `Thể thao ngoài trời` (+81), `Đồ thú cưng` (+100), cùng `Nội thất` (+187), `Trang trí nhà cửa` (+123), `Áo` (+79), `Cốc và bình` (+68), `Đồ bếp` (+40).
- **Đợt 5 + 5B (2026-11-26 · +1.093 ảnh mới phủ rộng 9 nhóm):**
  - Bổ sung mạnh `Nội thất` (+460), `Áo` (+183), `Phụ kiện` (+115), `Đồ bếp` (+110), `Mũ` (+100), `Thể thao ngoài trời` (+61), `Đồ thú cưng` (+44), `Quần đùi` (+16), `Đồ lót` (+4) kèm ưu tiên ảnh nguyên hộp/chưa khui.
- **Đợt 4 + 4B (2026-11-26 · +727 ảnh mới, dọn -344 ảnh lỗi cũ):**
  - Bổ sung ngách `Nội thất` & `Áo :: polo-shirts`, và soi sạch toàn bộ 1.597 ảnh cũ ở `Áo`, `Thể thao ngoài trời`, `Đồng phục` để gỡ 344 ảnh lỗi.
- **Đợt 1–3 (2026-11-25 · +1.457 ảnh mới, dọn -234 ảnh, chuyển 1 ảnh):**
  - Kiểm trùng 4 lớp (URL, `review_id`, MD5/SHA-256, pHash) và duyệt trực quan contact sheet, loại sạch 52 ảnh stock/editorial Pexels và 54 ảnh trùng cũ.
