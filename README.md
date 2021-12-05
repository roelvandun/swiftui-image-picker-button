# ImagePickerButton
An handy button for choosing the image picker source

## Usage
```swift
@State private var selectedUIImage: UIImage?
@State private var selectedImage: Image?

ImagePickerButton(
    selectedUIImage: $selectedUIImage,
    onPickerDismiss: {
        guard let uiImage = selectedUIImage else { return }
        selectedImage = Image(uiImage: uiImage)
    },
    content: {
        // an example of content
        ZStack {
            Image(systemName: "folder")
                .resizable()
                .aspectRatio(contentMode: .fit)
                .frame(width: 100, height: 100)
        }
        .contentShape(Rectangle())
    }
)
```
