# FileTypeDetector

[![Composer package](http://xn--e1adiijbgl.xn--p1acf/badge/wapmorgan/file-type-detector)](https://packagist.org/packages/wapmorgan/file-type-detector)
[![Latest Stable Version](https://poser.pugx.org/wapmorgan/file-type-detector/v/stable)](https://packagist.org/packages/wapmorgan/file-type-detector)
[![Total Downloads](https://poser.pugx.org/wapmorgan/file-type-detector/downloads)](https://packagist.org/packages/wapmorgan/file-type-detector)
[![Latest Unstable Version](https://poser.pugx.org/wapmorgan/file-type-detector/v/unstable)](https://packagist.org/packages/wapmorgan/file-type-detector)
[![License](https://poser.pugx.org/wapmorgan/file-type-detector/license)](https://packagist.org/packages/wapmorgan/file-type-detector)


### How to detect by file name
```php
$type = wapmorgan\FileTypeDetector\Detector::detectByFilename(...filename...);
```
`$type` will contain file type as an array like this:
```
[0] => Detector::AUDIO,
[1] => Detector::MP3
```
In case of failure it will contain `false`.

### How to detect by file content
```php
$type = wapmorgan\FileTypeDetector\Detector::detectByContent(...filename...);
// or
$type = wapmorgan\FileTypeDetector\Detector::detectByContent(...stream...);
```
`$type` can have the same values as described above.

## List of types
| Format            | In code                    |
|-------------------|----------------------------|
| **Audio**         | **Detector::AUDIO**        |
| .flac             | Detector::FLAC             |
| .wma              | Detector::WMA              |
| .amr              | Detector::AMR              |
| .mp3              | Detector::MP3              |
| .aac              | Detector::AAC              |
| .m3u              | Detector::M3U              |
| **Video**         | **Detector::VIDEO**        |
| .3gp              | Detector::THREE_GP         |
| .avi              | Detector::AVI              |
| .flv              | Detector::FLV              |
| .m4v              | Detector::M4V              |
| .mkv              | Detector::MKV              |
| .mov              | Detector::MOV              |
| .mpeg, .mpg       | Detector::MPEG             |
| **Images**        | **Detector::IMAGE**        |
| .jpeg, .jpg       | Detector::JPEG             |
| .bmp              | Detector::BMP              |
| .gif              | Detector::GIF              |
| .png              | Detector::PNG              |
| .tiff             | Detector::TIFF             |
| .psd              | Detector::PSD              |
| **Archives**      | **Detector::ARCHIVE**      |
| .bz2              | Detector::BZIP2            |
| .gz               | Detector::GZIP             |
| .xz               | Detector::LZMA2            |
| .7z               | Detector::SEVEN_ZIP        |
| .cab              | Detector::CAB              |
| .jar              | Detector::JAR              |
| .rar              | Detector::RAR              |
| .tar              | Detector::TAR              |
| .zip              | Detector::ZIP              |
| **Databases**     | **Detector::DATABASE**     |
| .mdb              | Detector::MDB              |
| .odb              | Detector::ODB              |
| **Documents**     | **Detector::DOCUMENT**     |
| .doc              | Detector::DOC              |
| .docx             | Detector::DOCX             |
| .html             | Detector::HTML             |
| .odt              | Detector::ODT              |
| .pdf              | Detector::PDF              |
| .rtf              | Detector::RTF              |
| .txt              | Detector::TXT              |
| .xml              | Detector::XML              |
| **Font-faces**    | **Detector::FONT**         |
| .otf              | Detector::OTF              |
| .ttf              | Detector::TTF              |
| **Executables**   | **Detector::APPLICATION**  |
| .apk              | Detector::APK              |
| .com              | Detector::COM              |
| .exe              | Detector::EXE              |
| **Presentations** | **Detector::PRESENTATION** |
| .ppt              | Detector::PPT              |
| .pptx             | Detector::PPTX             |
| .odp              | Detector::ODP              |
| **Spreadsheets**  | **Detector::SPREADSHEET**  |
| .ods              | Detector::ODS              |
| .xls              | Detector::XLS              |
| .xlsx             | Detector::XLSX             |
