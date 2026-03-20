import android.content.Context
import android.graphics.Canvas
import android.graphics.Color
import android.graphics.Paint
import android.view.View

class GameView(context: Context) : View(context) {

    private val paint = Paint()
    private var x = 100f

    override fun onDraw(canvas: Canvas) {
        super.onDraw(canvas)

        canvas.drawColor(Color.BLACK)

        paint.color = Color.WHITE
        canvas.drawRect(x, 200f, x + 100, 300f, paint)

        x += 5

        invalidate() // перерисовка
    }
}
