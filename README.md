# Flutter Note

## Flutter command
### Setup
- Clean and get package: f clean && f pub get && cd ios && rm -rf Pods && rm -rf Podfile.lock && arch -x86_64 pod install && cd ..
- Generate code: f pub run build_runner build --delete-conflicting-outputs && f pub run intl_utils:generate
### Unit Test
- Run test coverage: flutter test --coverage
- Remove file unuse: lcov --remove coverage/lcov.info 'lib/*/*/freezed.dart' 'lib/*/*.g.dart' 'lib/*/*.part.dart' 'lib//generated/*/*.dart' 'lib/core/*' 'lib/external/*' 'lib/presentation/common_widgets/*' 'lib/presentation/features/*' 'lib/config/*' 'lib/generated/*' 'lib/utils/*' 'lib/app.dart' 'lib/firebase_options.dart' 'lib/main_base.dart' 'lib/main_dev.dart' 'lib/main_mock.dart' 'lib/main_prod.dart' 'lib/main_qa.dart' 'lib/main_stg.dart' 'lib/injection/*' 'lib/main_stg.dart' 'lib/domain/entities/messages/*' 'lib/presentation/bloc/messages/*' -o coverage/lcov.info
- Generate test coverage html: genhtml coverage/lcov.info -o coverage/html
- Open test coverage: open coverage/html/index.html
