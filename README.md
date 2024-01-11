## TestLib_011124 (Bug link: https://github.com/dotnet/maui/issues/19804) 
- Use this library project in the consuming app.
- Add EmptyListMessage control in the page where you have used CollectionView and you want to show this message when collectionview is empty.
- You will notice that it will show the message but Image is not showing up. It gives below errors:

### Android error:
[Glide] Load failed for [no_records] with dimensions [606x2154]
[Glide] class com.bumptech.glide.load.engine.GlideException: Failed to load resource
[Glide] There were 3 root causes:
[Glide] java.io.FileNotFoundException(/no_records: open failed: ENOENT (No such file or directory))
[Glide] java.io.FileNotFoundException(open failed: ENOENT (No such file or directory))
[Glide] java.io.FileNotFoundException(open failed: ENOENT (No such file or directory))
[Glide]  call GlideException#logRootCauses(String) for more detail
[Glide]   Cause (1 of 3): class com.bumptech.glide.load.engine.GlideException: Fetching data failed, class java.io.InputStream, LOCAL
[Glide] There was 1 root cause:
[Glide] java.io.FileNotFoundException(/no_records: open failed: ENOENT (No such file or directory))

### iOS error:
Unable to load image file 'no_records'.
      System.InvalidOperationException: Unable to load image file.
Microsoft.Maui.FileImageSourceService: Warning: Unable to load image file 'no_records'.
System.InvalidOperationException: Unable to load image file.

