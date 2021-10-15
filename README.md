<!-- 本文件由 ./readme.make.md 自动生成，请不要直接修改此文件 -->

# try_catch

try call a async function , return value same as the function, on exception print error and ignore

## use

```dart
import 'package:try_catch/async.dart';

Future<int> test1() async {
  await Future.delayed(Duration(seconds: 3));
  throw Exception('test error');
}

Future<int> test2() async {
  await Future.delayed(Duration(seconds: 1));
  return 1;
}

void main() async {
  print('await sleep 3 seconds');
  print(await try_catch(() => test1())); //null
  print(await try_catch(() => test2())); //1
  print('done');
}

```
