# Note
* Dialog bottom sheet same iOS
``` private fun showDialogNotificationAction() {
        try {
            val sheetView: View =
                layoutInflater.inflate(R.layout.dialog_bottom_filter, null)
            mBottomDialogNotificationAction = BottomSheetDialog(this)
            mBottomDialogNotificationAction!!.setContentView(sheetView)
            mBottomDialogNotificationAction!!.show()

            // Remove default white color background
            // v28: android.support.design.R.id.design_bottom_sheet
            val bottomSheet =
                mBottomDialogNotificationAction!!.findViewById<View>(com.google.android.material.R.id.design_bottom_sheet) as FrameLayout?
            bottomSheet!!.background = null
        } catch (e: Exception) {
            e.printStackTrace()
        }
}```
