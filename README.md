# HƯỚNG DẪN TUÂN THỦ APP STORE
## 8386 - Ứng Dụng Dự Đoán Số Xổ Số

### 📋 CHECKLIST TUÂN THỦ APP STORE

#### ✅ **1. Privacy Policy (Bắt buộc)**
- [x] Tạo file `PRIVACY_POLICY.md`
- [x] Bao gồm tiếng Việt và tiếng Anh
- [x] Giải thích rõ việc thu thập dữ liệu
- [x] Liệt kê các bên thứ ba (Firebase/Google)
- [x] Quyền của người dùng
- [x] Cách liên hệ

#### ✅ **2. Terms of Service (Khuyến nghị)**
- [x] Tạo file `TERMS_OF_SERVICE.md`
- [x] Làm rõ tính chất giải trí
- [x] Hạn chế trách nhiệm
- [x] Quyền sở hữu trí tuệ

#### ✅ **3. App Information (Cần cập nhật)**
- [ ] Mô tả app trên App Store
- [ ] Keywords phù hợp
- [ ] Screenshots và video demo
- [ ] Category: Entertainment hoặc Lifestyle

### 🔧 **TÍCH HỢP VÀO APP**

#### **1. Thêm Privacy Policy vào App:**

Tạo file `PrivacyPolicyView.swift`:

```swift
import SwiftUI

struct PrivacyPolicyView: View {
    @Environment(\.presentationMode) var presentationMode
    
    var body: some View {
        NavigationView {
            ScrollView {
                VStack(alignment: .leading, spacing: 16) {
                    Text("Chính sách bảo mật")
                        .font(.title)
                        .fontWeight(.bold)
                    
                    Text("Nội dung chính sách bảo mật...")
                        .font(.body)
                    
                    // Thêm toàn bộ nội dung từ PRIVACY_POLICY.md
                }
                .padding()
            }
            .navigationTitle("Chính sách bảo mật")
            .navigationBarTitleDisplayMode(.inline)
            .navigationBarItems(trailing: Button("Đóng") {
                presentationMode.wrappedValue.dismiss()
            })
        }
    }
}
```

#### **2. Thêm vào Settings Menu:**

Trong `MainView.swift`, thêm:

```swift
NavigationLink(destination: PrivacyPolicyView()) {
    HStack {
        Image(systemName: "lock.shield")
        Text("Chính sách bảo mật")
    }
}
```

#### **3. Thêm vào Onboarding:**

Trong `OnboardingView.swift`, thêm checkbox:

```swift
HStack {
    Image(systemName: isAgreed ? "checkmark.square.fill" : "square")
        .foregroundColor(isAgreed ? .green : .gray)
    
    Text("Tôi đồng ý với ")
        .foregroundColor(.white)
    
    Button("Chính sách bảo mật") {
        showPrivacyPolicy = true
    }
    .foregroundColor(.blue)
    
    Text("và ")
        .foregroundColor(.white)
    
    Button("Điều khoản dịch vụ") {
        showTerms = true
    }
    .foregroundColor(.blue)
}
```

### 📱 **THÔNG TIN APP STORE**

#### **App Name:**
```
8386 - Dự Đoán Số Xổ Số
```

#### **Subtitle:**
```
AI Tử Vi & Số May Mắn
```

#### **Description (Tiếng Việt):**
```
🔮 8386 - Ứng dụng dự đoán số xổ số thông minh dựa trên AI và tử vi

✨ TÍNH NĂNG NỔI BẬT:
• Dự đoán số may mắn dựa trên tử vi cá nhân
• Tính toán cung hoàng đạo, ngũ hành, thiên can địa chi
• AI phân tích và đưa ra dự đoán chính xác
• Lưu trữ lịch sử dự đoán cá nhân
• Giao diện đẹp mắt, dễ sử dụng

🌟 CÁCH SỬ DỤNG:
1. Nhập ngày sinh và giới tính
2. AI tính toán tử vi cá nhân
3. Nhận dự đoán số may mắn hàng ngày
4. Lưu trữ và theo dõi kết quả

⚠️ LƯU Ý:
• Dự đoán chỉ mang tính chất giải trí
• Không đảm bảo 100% chính xác
• Sử dụng có trách nhiệm

🎯 PHÙ HỢP VỚI:
• Người yêu thích tử vi và chiêm tinh
• Người chơi xổ số muốn tham khảo
• Người quan tâm đến số học và may mắn
```

#### **Description (English):**
```
🔮 8386 - Smart lottery prediction app based on AI and horoscope

✨ KEY FEATURES:
• Lucky number predictions based on personal horoscope
• Calculate zodiac sign, five elements, heavenly stems, earthly branches
• AI analysis for accurate predictions
• Personal prediction history storage
• Beautiful and user-friendly interface

🌟 HOW TO USE:
1. Enter birth date and gender
2. AI calculates personal horoscope
3. Receive daily lucky number predictions
4. Store and track results

⚠️ NOTE:
• Predictions are for entertainment purposes only
• No 100% accuracy guarantee
• Use responsibly

🎯 PERFECT FOR:
• Horoscope and astrology enthusiasts
• Lottery players seeking reference
• People interested in numerology and luck
```

#### **Keywords:**
```
xổ số,dự đoán,tử vi,chiêm tinh,may mắn,số học,hoàng đạo,ngũ hành,lottery,prediction,horoscope,astrology,lucky,numbers
```

#### **Category:**
```
Entertainment
```

#### **Age Rating:**
```
4+ (Suitable for all ages)
```

### 🚀 **BƯỚC TIẾP THEO**

#### **1. Chuẩn bị tài khoản Developer:**
- [ ] Đăng ký Apple Developer Account ($99/năm)
- [ ] Tạo App ID cho 8386
- [ ] Thiết lập certificates và provisioning profiles

#### **2. Chuẩn bị assets:**
- [ ] App icon (1024x1024px)
- [ ] Screenshots cho các kích thước màn hình
- [ ] App preview video (khuyến nghị)

#### **3. Test và review:**
- [ ] Test trên nhiều thiết bị iOS
- [ ] Kiểm tra tất cả tính năng
- [ ] Đảm bảo không crash
- [ ] Test với các kích thước màn hình khác nhau

#### **4. Submit lên App Store:**
- [ ] Upload build lên App Store Connect
- [ ] Điền đầy đủ thông tin app
- [ ] Upload screenshots và metadata
- [ ] Submit for review

### 📞 **LIÊN HỆ HỖ TRỢ**

Nếu cần hỗ trợ thêm về việc submit app:

**Email**: [Email của bạn]
**Website**: [Website của bạn nếu có]
**Support**: [Thông tin hỗ trợ]

---

**Lưu ý quan trọng:**
- Đảm bảo thay thế tất cả placeholder [Email], [Địa chỉ], [Số điện thoại] bằng thông tin thực
- Review lại chính sách bảo mật và điều khoản dịch vụ trước khi submit
- Kiểm tra kỹ tính năng "dự đoán" để đảm bảo tuân thủ guidelines của Apple về cờ bạc



