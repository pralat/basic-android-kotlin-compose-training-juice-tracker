# Fix unresolved reference 'color' and 'R' errors

The build is failing due to incorrect or missing `R` imports in `ColorSpinnerRow.kt` and `RatingInputRow.kt`.

## Proposed Changes

### [app]

#### [MODIFY] [ColorSpinnerRow.kt](file:///Users/mark/StudioProjects/basic-android-kotlin-compose-training-juice-tracker/app/src/main/java/com/example/juicetracker/ui/bottomsheet/ColorSpinnerRow.kt)
- Replace `import android.R` with `import com.example.juicetracker.R` to access app-specific string resources.
- Update `R.layout.simple_spinner_dropdown_item` to `android.R.layout.simple_spinner_dropdown_item` since this is a system resource.

#### [MODIFY] [RatingInputRow.kt](file:///Users/mark/StudioProjects/basic-android-kotlin-compose-training-juice-tracker/app/src/main/java/com/example/juicetracker/ui/bottomsheet/RatingInputRow.kt)
- Add `import com.example.juicetracker.R` to resolve the `R` reference.

## Verification Plan

### Automated Tests
- Run `./gradlew :app:compileDebugKotlin` to verify that the project builds successfully.
