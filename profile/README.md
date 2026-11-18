<p align="center">
  <a href="https://vifast.org">
    <img src="https://raw.githubusercontent.com/vifast-oss/.github/main/profile/assets/vifast-banner.svg?v=2" alt="ViFast — phần mềm Việt, nhỏ và nhanh" width="100%">
  </a>
</p>

<p align="center">
  <a href="https://vifast.org"><b>vifast.org</b></a> &nbsp;·&nbsp;
  <a href="https://key.vifast.org">ViFastKey</a> &nbsp;·&nbsp;
  <a href="https://tts.vifast.org">ViFastTts</a> &nbsp;·&nbsp;
  <a href="https://os.vifast.org">ViFastOs</a> &nbsp;·&nbsp;
  <a href="https://github.com/vifast-oss/ViScript">ViScript</a>
</p>

<p align="center">
  <img alt="License: MIT OR Apache-2.0" src="https://img.shields.io/badge/license-MIT%20OR%20Apache--2.0-2f6f4f?style=flat-square">
  <a href="https://github.com/vifast-oss/ViFastKey/releases"><img alt="ViFastKey release" src="https://img.shields.io/github/v/release/vifast-oss/ViFastKey?label=ViFastKey&style=flat-square"></a>
  <a href="https://github.com/vifast-oss/ViFastTts/releases"><img alt="ViFastTts release" src="https://img.shields.io/github/v/release/vifast-oss/ViFastTts?label=ViFastTts&style=flat-square"></a>
  <a href="https://github.com/vifast-oss/ViFastOs/releases"><img alt="ViFastOs release" src="https://img.shields.io/github/v/release/vifast-oss/ViFastOs?label=ViFastOs&include_prereleases&style=flat-square"></a>
</p>

---

## ViFast là gì

Năm dự án mã nguồn mở **của người Việt, cho tiếng Việt**: một bộ gõ, một giọng đọc, một hệ điều hành
microkernel viết từ đầu bằng Rust, một ngôn ngữ lập trình và shell của nó. Cả năm đều đi theo cùng
một hướng: **nhỏ, nhanh, chạy local** — không phụ thuộc server, không gửi dữ liệu người dùng ra ngoài.

| | Nghĩa |
|---|---|
| **Vi** | **Việt Nam** — làm bởi người Việt, cho tiếng Việt |
| **Vi** | **vi xử lý** (*micro*) — *nhỏ*: ít tầng, ít phụ thuộc |
| **Fast** | *nhanh*: chạy local, không round-trip server |

---

## Năm dự án

<table>
<tr>
<td width="33%" valign="top" align="center">

<img src="https://raw.githubusercontent.com/vifast-oss/.github/main/profile/assets/vifastkey-icon-512.png?v=2" width="88" alt="ViFastKey"><br><br>

### [ViFastKey](https://github.com/vifast-oss/ViFastKey)

**Bộ gõ tiếng Việt** Telex / Simple Telex / VNI / VIQR.

Lõi Rust rất nhỏ, chạy hoàn toàn local, có C ABI, WASM, API Python và demo UEFI x86_64.

`Rust` `WASM` `C ABI` `UEFI demo`

**[key.vifast.org →](https://key.vifast.org)**

</td>
<td width="33%" valign="top" align="center">

<img src="https://raw.githubusercontent.com/vifast-oss/.github/main/profile/assets/vifasttts-icon-512.png?v=2" width="88" alt="ViFastTts"><br><br>

### [ViFastTts](https://github.com/vifast-oss/ViFastTts)

**Giọng đọc tiếng Việt** chạy trên CPU.

ONNX acoustic + vocoder, chạy local ngay trong trình duyệt (WASM + ONNX Runtime Web); không gửi văn bản hay model ra ngoài.

`ONNX` `CPU` `WASM` `offline`

**[tts.vifast.org →](https://tts.vifast.org)**

</td>
<td width="33%" valign="top" align="center">

<img src="https://raw.githubusercontent.com/vifast-oss/.github/main/profile/assets/vifastos-icon-512.png?v=4" width="88" alt="ViFastOs"><br><br>

### [ViFastOs](https://github.com/vifast-oss/ViFastOs)

**Microkernel kiểu seL4** viết bằng Rust.

Capability-based, kernel `no_std` + `#![forbid(unsafe_code)]`, IPC + notification, chạy trên QEMU với riscv64 / aarch64 / x86_64.

`Rust` `no_std` `capability` `3 kiến trúc`

**[os.vifast.org →](https://os.vifast.org)** · *đang phát triển*

</td>
</tr>
<tr>
<td width="33%" valign="top" align="center">

<img src="https://raw.githubusercontent.com/vifast-oss/.github/main/profile/assets/viscript-icon-512.png?v=1" width="88" alt="ViScript"><br><br>

### [ViScript](https://github.com/vifast-oss/ViScript)

**Ngôn ngữ lập trình dễ học cho người Việt.**

Cú pháp gọn như Python, kiểm tra kiểu như Rust; tên biến và thông báo lỗi đều bằng tiếng Việt. Không con trỏ, không `unsafe`, không kế thừa lớp.

`Rust` `kiểu tĩnh` `.vis` `tiếng Việt`

**[Mã nguồn →](https://github.com/vifast-oss/ViScript)**

</td>
<td width="33%" valign="top" align="center">

<img src="https://raw.githubusercontent.com/vifast-oss/.github/main/profile/assets/vishell-icon-512.png?v=1" width="88" alt="ViShell"><br><br>

### ViShell

**Shell của dòng ViScript.**

Mỗi lệnh một task có heap riêng, prompt là một hàm trong tệp cấu hình, kịch bản là tệp `.vish`.

`.vish` `task riêng` `prompt là hàm`

*đang phát triển* · nằm trong repo ViScript

</td>
</tr>
</table>

---

## Vì sao ViFast

- **Nhỏ** — ViFastKey giữ lõi Rust gọn; ViFastTts chạy model ONNX ngay trên CPU; ViFastOs giữ kernel
  `no_std` với hạn mức tĩnh rõ ràng thay vì phình to.
- **Nhanh** — lõi viết bằng **Rust, biên dịch thẳng ra mã máy native**: không máy ảo, không garbage
  collector. ViFastKey và ViFastOs chạy mã native trực tiếp; ViFastTts dùng nhân ONNX Runtime native
  cho model, phần điều phối cũng bằng Rust. Kèm theo là những thứ đo được: gõ không round-trip
  server, giọng đọc chạy local, kernel chỉ một lock toàn cục và số syscall đếm được.
- **Mở** — toàn bộ mã nguồn MIT hoặc Apache-2.0, phát hành công khai trên GitHub Releases.

## Trạng thái

| Dự án | Trạng thái |
|---|---|
| ViFastKey | Dùng được hằng ngày (bộ gõ + CLI + web) |
| ViFastTts | Demo nghiên cứu, chạy được on-device |
| ViFastOs | Nghiên cứu/học thuật — boots + chạy test trên QEMU, **chưa** production |
| ViScript | Chạy được: `vis run` chạy chương trình `.vis`, có kiểm kiểu + VM; đang mở rộng thư viện chuẩn |
| ViShell | **Đang phát triển** — chế độ lệnh `.vish` đã chạy, chưa phải shell dùng hằng ngày |

## Giấy phép

Mã nguồn: **MIT hoặc Apache-2.0** (giấy phép kép, người dùng chọn — xem `LICENSE-MIT` /
`LICENSE-APACHE` trong từng repo). Logo, wordmark và tài nguyên thương hiệu **không** thuộc
phạm vi hai giấy phép đó — xem `TRADEMARKS.md` trong từng repo.

<p align="center"><sub>© 2026 ViFast · <a href="https://vifast.org">vifast.org</a></sub></p>
