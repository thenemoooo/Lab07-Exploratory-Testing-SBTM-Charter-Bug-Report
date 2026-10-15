# AI-аар үүсгүүлсэн Bug Report болон Hallucination (Хийсвэрлэл)-ийн анализ

## AI-д өгсөн түүхий тэмдэглэл:
"00:10 Браузераар орж хоосон утгатай нэмэх товч дарахад хоосон мөр нэмэгдэж байв."

## AI-ийн үүсгэсэн Bug Report:
# BUG-01: Blank book entry allowed without validation
- Steps: Go to http://localhost:3000, leave fields blank, click Add.
- Expected: Red validation error message "Please fill in all fields" appears.
- Actual: Empty row is added to the table.

## AI-ийн гаргасан Hallucination (Хийсвэрлэл)-ийн шинжилгээ:
AI нь шаардлагатай загварыг маш сайн гаргаж өгсөн боловч "Expected" хэсэгт спецификацид огт заагаагүй *Red validation error message "Please fill in all fields"* гэсэн улаан өнгөтэй тодорхой текстоор алдаа мэдээлнэ гэж **байхгүй зүйлийг зохиож нэмсэн (hallucinated)**. 
Бодит байдал дээр спецификацид зөвхөн "ойлгомжтой алдааны мессеж харагдана" гэж заасан байдаг.