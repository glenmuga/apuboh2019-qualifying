# Stone

We are given a .zip file, we can extract it using command `unzip set_in_stone.zip`. We will get a `.png` file. 

Opening the `.png` file show a picture with Roman Numeral characters. 

We start by using command `file set_in_stone.png` to see the file format. It shows it is a PNG file. Next we use `exiftool set_in_stone.png` to look at the metadata of the picture but there is nothing interesting in it. We also perform `binwalk set_in_stone.png` to look for any embedded files but there is nothing interesting again.

Therefore, the flag is likely writtien in Roman Numeral characters. Transcribe the picture and you will get `XCVII CXII CXVII XCVIII CXI CIV L  XLVIII XLIX LVII CXXIII XCVII CX  XCIX XLIX LI CX CXVI XCV CXIV LI CVIII XLIX XCIX LIII CXXV`

We can just google for roman numeral cipher and it will show roman numerals to caesar cipher. I used [this](https://v2.cryptii.com/roman-numerals/caesar) to decode it.

The result will be the flag.

### Flag

Flag: `apuboh2019{anc13nt_r3l1cs}`
