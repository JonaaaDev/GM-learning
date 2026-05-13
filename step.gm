// Delta time
var dt = delta_time / 1000000;


// ========================
// CLICK DESTINO
// ========================

if (mouse_check_button(mb_left)) {
    target_x = mouse_x;
    target_y = mouse_y;
}


// ========================
// MOVIMIENTO
// ========================

var dist = point_distance(real_x, real_y, target_x, target_y);

if (dist > 2) {

    dir = point_direction(real_x, real_y, target_x, target_y);

    var move = _speed * dt;

    move = min(move, dist);

    real_x += lengthdir_x(move, dir);
    real_y += lengthdir_y(move, dir);
}


// ========================
// ANIMACION FLOTANTE
// ========================

x = real_x;

if (dist <= 2) {

    // flotación solo quieto
    float_timer += dt * float_speed;

    y = real_y + sin(float_timer) * float_amount;

} else {

    // mientras se mueve
    y = real_y;

}
// ========================
// SPRITE DIRECCIONAL
// ========================

dir = dir mod 360;

var grados_por_frame = 360 / total_frames;

image_index = floor(dir / grados_por_frame);
