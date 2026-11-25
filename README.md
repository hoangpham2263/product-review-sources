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

- **Tổng số ảnh (`manifest.json` & cây thư mục):** **4.536 ảnh** (~**979,5 MB**) thuộc **12 nhóm** (tất cả `enabled: true`)
- **Tổng bản ghi `catalog.json`:** **4.172** (`review`: 4.128 · `customer_gallery`: 38 · `original`: 6 · `stock/listing/editorial`: **0**)
- **Kiểm tra trùng lặp:** **0 trùng MD5** toàn repo · **0 trùng SHA-256** toàn `catalog.json`

### Thống kê theo nhóm & danh mục

| Nhóm (`source_group`) | Số ảnh | Trong `catalog.json` | Dung lượng | Chi tiết danh mục (`category`) |
| --- | ---: | ---: | ---: | --- |
| **Áo** | **1.408** | 1.408 | 293,4 MB | `tees-hoodies` (1.235), `polo-shirts` (159), `team-jerseys` (14) |
| **Nội thất** | **1.331** | 967 *(364 ảnh cũ chưa có bản ghi catalog)* | 421,8 MB | `dining-tables` (155), `wall-neon` (122), `desks` (80), `sofas` (75), `bookshelves` (73), `coffee-tables` (72), `chairs` (69), `side-tables` (67), `beds` (52), `cabinets` (41), `console-tables` (31), `floor-lamps` (28), `media-consoles` (27), `dressers` (23), `sideboards` (20), `mirrors` (9), `rugs` (7), `ceiling-lights` (6), `ottomans` (6), `table-lamps` (4) |
| **Trang trí nhà cửa** | **784** | 784 | 139,6 MB | `ornaments` (254), `garden-flag` (215), `pillows` (163), `doormats` (79), `canvas` (32), `blankets` (18), `posters` (9), `memorial-stone` (6), `home-decor` (5), `acrylic-plaque` (3) |
| **Cốc và bình** | **670** | 670 | 74,2 MB | `drinkware` (670) |
| **Phụ kiện** | **143** | 143 | 18,8 MB | `keychains` (76), `jewelry` (66), `neckties` (1) |
| **Đồ thú cưng** | **75** | 75 | 11,4 MB | `pet-bowls` (47), `bandana` (19), `pet-food-mat` (9) |
| **Thể thao ngoài trời** | **30** | 30 | 5,2 MB | `outdoor-sports` (30) |
| **Mũ** | **27** | 27 | 3,7 MB | `hats` (27) |
| **Đồng phục** | **25** | 25 | 3,7 MB | `medical-scrubs` (25) |
| **Đồ lót** | **19** | 19 | 3,0 MB | `underwear` (19) |
| **Đồ bếp** | **13** | 13 | 2,7 MB | `oven-mitts` (13) |
| **Quần đùi** | **11** | 11 | 2,0 MB | `hawaiian-beachwear` (11) |
| **Tổng cộng** | **4.536** | **4.172** | **979,5 MB** | |

### Nhật ký cập nhật gần nhất (2026-11-25)

- **Bổ sung +856 ảnh review thật** từ Judge.me (đã kiểm trùng URL, `review_id`, MD5, SHA-256, perceptual hash `16×16 dHash ≤ 20/256` và duyệt trực quan contact sheet):
  - **`Áo` (+246 ảnh):** tập trung người thật mặc áo polo/áo thun và ảnh còn trong bì / gấp vừa nhận hàng (`usuckatgolf.com`, `sunrisewear.com`, `miersports.com`, `kingdomofwhite.com`, `lexandyork.com`, `imaxfashions.com`, `nostrumfashion.com`, `madeforfreemasons.com`, `iamseawolf.eu`, `anetik.com`, `soneven.com`, `freesoldier.com`, `bairnsdalehorsecentre.com.au`).
  - **`Nội thất` (+610 ảnh):** nội thất gỗ trong nhà và cảnh tường/phòng/bar/cafe/salon/shop/tiệc cưới (`furniselan.com`, `unikito.com`, `timbergirl.com`, `showhome-furniture.com`, `bysuryavanshi.com`, `dusk.com`, `eurekaergonomic.com`, `vingliwebsite.myshopify.com`, `hasuit.com`, `kaguyasu.com`, `anzhap.com`, `furnisquare.com`, `fastneonsigns.com`, `neonsignslights.com`, `neonsignkingdom.com`, `makeneon.com`, `luckyneon.com`, `shimmerandconfetti.com`, `nuwaveneon.com`).
- **Dọn dẹp & chuyển danh mục (-234 ảnh, chuyển 1 ảnh):**
  - Gỡ **52 ảnh stock/giả/catalog/editorial** (Pexels model trong `Áo` và `Thể thao ngoài trời`, ảnh listing/editorial trong `Nội thất`).
  - Gỡ **51 ảnh trùng MD5** và **3 ảnh trùng pHash** tồn đọng trong `Nội thất`.
  - Chuyển **1 ảnh chó đeo khăn bandana** từ `Áo` sang `Đồ thú cưng` (`f9549680-fdd3-423d-aa1c-bf7d2665a38c.jpg`).
  - Gỡ **12 ảnh chó thuần không có áo** + **17 ảnh không dùng được** trong `Áo`, **77 ảnh ngoài trời/cắm trại/xe/sân vườn** + **20 ảnh hộp/hỏng/tối** trong `Nội thất`, **4 ảnh ghép/mờ** trong `Đồng phục`, **1 ảnh dính banner** trong `Thể thao ngoài trời`.

### Điểm còn mỏng / hướng bổ sung tiếp

- **Ảnh còn trong bì / vừa khui hàng thật:** hiện mới có ~50–60 ảnh trong `Áo`, có thể bổ sung thêm.
- **Một số ngách `Nội thất` gỗ:** `console-tables` (31), `media-consoles` (27), `dressers` (23), `sideboards` (20), `mirrors` (9), `rugs` (7), `table-lamps` (4).
- **Nhóm `Áo` cũ (~1.100 ảnh import đợt đầu):** mới duyệt trực quan một phần; có thể tiếp tục rà contact sheet để lọc hết ảnh lẫn thú cưng/cận hình in còn sót.

