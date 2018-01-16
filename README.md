# imgPinch
压缩图片

# use
 var files = e.target.files || e.dataTransfer.files
  var imagePinch = new ImagePinch({
    file: files[0],
    toHeight: 400,
    maxSize: 1024,
    success: function(file) {
      vm.file = file
      var reader = new FileReader()
      reader.onload = (e) => {
        vm.image = e.target.result
      }
      reader.readAsDataURL(file)
    }
  })
  imagePinch.pinch()
