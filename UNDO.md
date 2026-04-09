# WRITE UP
kết nối vào `nc foggy-cliff.picoctf.net 65204`
sẽ xuất hiện một chuỗi

`KTJxNW85NjQ1LWZhMDFnQHplMHNmYTRlRy1nazNnLXRhMWZlcmlyRShTR1BicHZj`

có thể thấy đây là chuỗi mã hóa base64

decode bằng `base64 -d`

`)2q5o9645-fa01g@ze0sfa4eG-gk3g-ta1ferirE(SGPbpvc` 

theo đề bài sử dung `rev` để đảo ngược chuỗi

`cvpbPGS(Eriref1at-g3kg-Ge4afs0ez@g10af-5469o5q2)`

tiếp theo thay thế các ký tự '-' thành '_'

`tr '-' '_'`

`cvpbPGS(Eriref1at_g3kg_Ge4afs0ez@g10af_5469o5q2)`

sau đó thay thế ký tự '()' sang '{}'

`tr '()' '{}'`

`cvpbPGS{Eriref1at_g3kg_Ge4afs0ez@g10af_5469o5q2}`

cuối cùng kéo các ký tự sang 13 bước bên phải (ROT13)

`tr 'a-zA-Z' 'n-za-mN-ZA-M`

## FLAG

`picoCTF{Revers1ng_t3xt_Tr4nsf0rm@t10ns_5469b5d2}`





