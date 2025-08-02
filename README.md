<h1 align="center" style="font-weight:bold;">
  <img src="https://media.tenor.com/SrQO6J_VT-4AAAAj/cemetery-divider.gif" /> 
  <span style="color:#708090;">RUNNERVANIA</span>
  <img src="https://media.tenor.com/SrQO6J_VT-4AAAAj/cemetery-divider.gif" />
</h1>

<h3 align="center" style="color:#708090;">Maria Jose Vazquez Romano</h3>

<p align="center">
  <img src="https://media1.tenor.com/m/DqyyEmRmJK0AAAAC/flowers-cherry-blossom.gif" />
</p>

<div align="center">
  <p>Juego inspirado en los juegos, serie, peliculas y libros de dracula y  castelvania .</p>
  <p>Una mecánica que predomina en el primer nivel es la urgencia por alcanzar la finalidad del mapa a la derecha, para escapar de un muro de murciélagos. De ahí lo "runner", además el camino está habitado por criaturas del averno, que complicarán la huida de nuestro personaje.</p>
</div>

<h1></h1>
<h1 align="center" style="font-weight:bold; color:#708090;">Assets y audio</h1>

<h3 align="center" style="color:#708090;">Imágenes</h3>
<p align="center">
  <img src="https://img.itch.zone/aW1hZ2UvNDI4MDMyLzIxMzkwODkucG5n/original/3XaCEY.png" width="45%"/>
  <img src="https://img.itch.zone/aW1hZ2UvNDI4MDMyLzEwNjU4ODYzLnBuZw==/original/DTf%2FAx.png" width="45%"/>
  <img src="https://img.itch.zone/aW1hZ2UvNjQ4MjgvMjkzMDYyLnBuZw==/original/NAoaas.png" width="45%"/>
  <img src="https://img.itch.zone/aW1hZ2UvNDcyNzM1LzI0MjM2MTkucG5n/original/NQR89B.png" width="45%"/>
  <img src="https://img.itch.zone/aW1hZ2UvNDcyNzM1LzI0MjM2MjIucG5n/original/3yoH1G.png" width="45%"/>
  <img src="https://img.itch.zone/aW1hZ2UvMjYwNTg5Mi8yMDQxNTAxNy5naWY=/original/76cylp.gif" width="45%"/>
</p>

<h3 align="center" style="color:#708090;">Música</h3>
<div align="center">
  <a href="https://youtu.be/D4uq8p8p_5I"><img src="https://img.youtube.com/vi/D4uq8p8p_5I/mqdefault.jpg" alt="Canción 1" width="30%"/></a>
  <a href="https://youtu.be/4fu68WjVJ0o"><img src="https://img.youtube.com/vi/4fu68WjVJ0o/mqdefault.jpg" alt="Canción 2" width="30%"/></a>
  <a href="https://youtu.be/wYCdL1TENBI"><img src="https://img.youtube.com/vi/wYCdL1TENBI/mqdefault.jpg" alt="Canción 3" width="30%"/></a>
</div>

<div align="center">
  <p>Niveles //////////// Fin de nivel /////////// Game Over</p>
</div>

<h1></h1>
<h1 align="center" style="font-weight:bold; color:#708090;">Escenas</h1>

<h3 align="center" style="color:#708090;">Nivel 1</h3>
<p align="center"><img src="https://alejandrom123.sg-host.com/wp-content/uploads/2025/07/esc1.png" width="70%"/></p>
<p align="center">El primer nivel, tiene enemigos, monedas y pociones, además de la distinción del muro de murcielagos que le pone "runner" al nombre del juego.</p>

<h3 align="center" style="color:#708090;">Nivel 2</h3>
<p align="center"><img src="https://alejandrom123.sg-host.com/wp-content/uploads/2025/07/esc2.png" width="70%"/></p>
<p align="center">El segundo nivel , tiene enemigos, monedas y pociones, no perdiendo su escencia de "comido por la madre naturaleza". Además tiene el texto de finalización del juego.</p>

<h3 align="center" style="color:#708090;">Personaje</h3>
<p align="center"><img src="https://alejandrom123.sg-host.com/wp-content/uploads/2025/07/esc31.png" width="70%"/></p>
<p align="center">La escena del personaje contiene la mayoría del código de juego con poco más de 200 líneas, ahí se encuentran contenidas la mayoría de funcionalidades del juego.</p>

<h3 align="center" style="color:#708090;">Enemigos</h3>
<p align="center"><img src="https://alejandrom123.sg-host.com/wp-content/uploads/2025/07/esc4.png" width="70%"/></p>
<p align="center">La escena de los enemigos es la misma siempre, cambia solamente el tipo de enemigo en formato lista.</p>

<h3 align="center" style="color:#708090;">Plataformas</h3>
<p align="center"><img src="https://alejandrom123.sg-host.com/wp-content/uploads/2025/07/esc7.png" width="70%"/></p>
<p align="center">Las plataformas del juego son la misma escena copypasteada y con el tilemap/collision cambiadas.</p>


<h3 align="center" style="color:#708090;">Moneda</h3>
<p align="center"><img src="https://alejandrom123.sg-host.com/wp-content/uploads/2025/07/esc8.png" width="70%"/></p>
<p align="center">Escena necesaria para que el jugador pueda recoger monedas.</p>

<h3 align="center" style="color:#708090;">Poción</h3>
<p align="center"><img src="https://alejandrom123.sg-host.com/wp-content/uploads/2025/07/esc5.png" width="70%"/></p>
<p align="center">Escena necesaria para que el jugador pueda recoger pociones y le suba la vida</p>

<h1></h1>
<h1 align="center" style="font-weight:bold; color:#708090;">Códigos relevantes</h1>

<details>
  <summary style="color:#708090;">Código del personaje</summary>
extends CharacterBody2D

# Propiedades de movimiento
var velocidad = 200
var brinco = -400
var gravedad = 1000

# Referencias y estado del jugador
@onready var sprite = $AnimatedSprite2D
var ultima_direccion = 1  
var vidas = 3
var puede_moverse := true
var recibe_daño := false
var monedas := 0
var invulnerable := false
@onready var label_monedas: Label = $Camera2D/ui/MonedaNum

func _ready():
	# Configuración inicial
	add_to_group("jugador")
	AnimVidas()  # Actualizar UI de vidas
	$musica/musiquita.play()
	$Camera2D/ui/GameOver.visible = false
	$Camera2D/ui/end.visible = false
	set_physics_process(true)
	$"Camera2D/ui/Panel-transparent-center-019".modulate.a = 0.5

func _physics_process(delta):
	if puede_moverse:
		# Movimiento basado en input
		var direccion = Input.get_axis("ui_left", "ui_right")
		velocity.x = direccion * velocidad
		
		# Gravedad y salto
		if not is_on_floor():
			velocity.y += gravedad * delta
		if Input.is_action_just_pressed("ui_up") and is_on_floor():
			velocity.y = brinco
	else:
		if not is_on_floor():
			velocity.y += gravedad * delta

	move_and_slide()
	
	if puede_moverse:
		actualizar_animaciones(Input.get_axis("ui_left", "ui_right"))

func actualizar_animaciones(direccion):
	"""
	Controla las animaciones del jugador según su estado y dirección.
	"""
	if recibe_daño:
		return
	
	if direccion != 0:
		ultima_direccion = direccion
	if not is_on_floor():
		if velocity.y < 0:
			sprite.play("salto")
		else:
			sprite.play("caida")
	else:
		if direccion == 0:
			sprite.play("idle")
		else:
			sprite.play("derecha")
	
	sprite.flip_h = ultima_direccion < 0

func ReducirVidas() -> void:
	"""
	Maneja la lógica de reducción de vidas con estados de invulnerabilidad.
	Incluye efectos visuales y sonoros.
	"""
	if invulnerable == true:
		return
	if vidas > 1 and invulnerable == false:
		# Lógica para daño normal
		vidas -= 1
		AnimVidas()
		invulnerable = true
		puede_moverse = false
		recibe_daño = true
		sprite.play("daño")
		velocity = Vector2(-ultima_direccion * 250, -100)  # Retroceso
		await get_tree().create_timer(0.3).timeout
		recibe_daño = false
		puede_moverse = true
		AnimDaño()
		await get_tree().create_timer(0.2).timeout
		invulnerable = false
	else:
		# Lógica para muerte del jugador
		vidas -= 1
		$musica/musiquita.stop()
		$musica/gameover.play()
		$Camera2D/ui/GameOver.visible = true
		AnimVidas()
		puede_moverse = false
		invulnerable = true
		set_physics_process(false)
		sprite.play("daño")
		await get_tree().create_timer(0.5).timeout
		sprite.play("muerte")
		await get_tree().create_timer(1.0).timeout
		sprite.visible = false
		await get_tree().create_timer(2.5).timeout
		get_tree().reload_current_scene()

func AnimDaño():
	"""
	Efecto visual de parpadeo al recibir daño.
	"""
	sprite.visible = false
	await get_tree().create_timer(0.1).timeout
	sprite.visible = true
	await get_tree().create_timer(0.1).timeout
	sprite.visible = false
	await get_tree().create_timer(0.1).timeout
	sprite.visible = true
	await get_tree().create_timer(0.1).timeout
	sprite.visible = false
	await get_tree().create_timer(0.1).timeout
	sprite.visible = true

func AnimVidas():
	"""
	Actualiza la UI de vidas según la cantidad actual.
	"""
	if vidas == 3:
		$Camera2D/ui/vida_tres.visible = true
		$Camera2D/ui/vida_dos.visible = true
		$Camera2D/ui/vida_uno.visible = true
		$Camera2D/ui/sano.visible = true
	elif vidas == 2:
		$Camera2D/ui/vida_tres.visible = false
		$Camera2D/ui/vida_dos.visible = true
		$Camera2D/ui/vida_uno.visible = true
		$Camera2D/ui/sano.visible = false
	elif vidas == 1:
		$Camera2D/ui/vida_tres.visible = false
		$Camera2D/ui/vida_dos.visible = false
		$Camera2D/ui/vida_uno.visible = true
		$Camera2D/ui/sano.visible = false
		$Camera2D/ui/herido.visible = false
	elif vidas <= 0:
		$Camera2D/ui/vida_tres.visible = false
		$Camera2D/ui/vida_dos.visible = false
		$Camera2D/ui/vida_uno.visible = false
		$Camera2D/ui/sano.visible = false
		$Camera2D/ui/herido.visible = false
		$Camera2D/ui/moribundo.visible = false

func agregar_moneda():
	"""
	Incrementa el contador de monedas y actualiza la UI.
	"""
	monedas += 1
	label_monedas.text = str(monedas)

func total_mon():
	"""
	Muestra la pantalla de fin de nivel con el total de monedas.
	Incluye efecto de parpadeo en el texto.
	"""
	$Camera2D/ui/end.visible = true
	$Camera2D/ui/end/Total_monedas.text = "Monedas obtenidas: %d" % monedas
	$Camera2D/ui/end/monedas_nivel.text = "26 monedas en el nivel"
	$Camera2D/ui/end/monedas_nivel.visible = false
	# Secuencia de parpadeo (repetida varias veces)
	[...]

# Señales y colisiones
func _on_reset_body_entered(body: Node2D) -> void:
	if is_in_group("jugador"):
		vidas -= 3
		ReducirVidas()

func _on_puerta_body_entered(body: Node2D) -> void:
	# Transición de nivel
	$musica/musiquita.stop()
	$musica/stage.play()
	invulnerable = true
	puede_moverse = false
	sprite.position = Vector2(5,-30)
	await get_tree().create_timer(.15).timeout
	sprite.visible = false
	total_mon()
	await get_tree().create_timer(4.35).timeout
	get_tree().change_scene_to_file("res://Assets/interior/node_2d.tscn")

func _on_hitbox_area_entered(area: Area2D) -> void:
	if area.is_in_group("dmgbox"):
		ReducirVidas()

func _on_murci_body_entered(body: Node2D) -> void:
	if body.is_in_group("jugador"):
		vidas -= 3
		ReducirVidas()
</details>

<p align="center">
  <img src="https://media.tenor.com/bhxZ5O_Xnq8AAAAj/page-divider-glittery.gif" />
</p>

<details>
  <summary style="color:#708090;">Código de los enemigos</summary>
extends CharacterBody2D

# Definición de tipos de enemigos mediante enumeración
enum EnemType {moco, ghost, ghoul, skeleton}

# Propiedades exportadas para configuración en el editor
@export var velocidad := 60
@export var gravedad := 1000
@export var patrulla := 50
@export var daño := 1
@export var type: EnemType = EnemType.moco

# Referencias a nodos hijos
@onready var sprite_enemigo = $AnimatedSprite2D
@onready var sprite_enemigo_gd = $grandes

# Variables de estado
var direction := -1
var start_position := Vector2.ZERO

func _ready():
	start_position = global_position
	ActuMons()  # Configuración inicial según tipo de enemigo

func ActuMons():
	"""
	Configura las propiedades del enemigo según su tipo.
	Incluye animaciones, gravedad, velocidad y ajustes visuales.
	"""
	match type:
		EnemType.moco:
			sprite_enemigo.play("moco")
			velocidad = velocidad * .6
			$grandes.visible = false
		EnemType.ghost:
			sprite_enemigo.play("ghost")
			gravedad = 0  # Fantasma no afectado por gravedad
			$dmgbox.scale = Vector2(0.8, 0.8)
			$CollisionShape2D.disabled = true
			$grandes.visible = false
		EnemType.ghoul:
			sprite_enemigo_gd.play("ghoul")
			velocidad = 120
			patrulla = 80
			$AnimatedSprite2D.visible = false
			sprite_enemigo_gd.position = Vector2(0, -15)
		EnemType.skeleton:
			sprite_enemigo_gd.play("skeleton")
			patrulla = patrulla * .5
			$AnimatedSprite2D.visible = false

func _physics_process(delta):
	# Movimiento horizontal
	velocity.x = direction * velocidad
	
	# Aplicar gravedad si no está en el suelo
	if not is_on_floor():
		velocity.y += gravedad * delta
	else:
		velocity.y = 0
	
	move_and_slide()  # Movimiento real del personaje
	
	# Lógica de patrulla (cambio de dirección al alcanzar límite)
	if abs(global_position.x - start_position.x) > patrulla:
		direction *= -1
		# Voltear sprites según dirección
		sprite_enemigo.flip_h = direction > 0
		sprite_enemigo_gd.flip_h = direction > 0

func _on_HurtBox_area_entered(area):
	# Detección de ataques del jugador
	if area.is_in_group("player_attack"):
		die()

func die():
	# Animación de muerte y eliminación del enemigo
	sprite_enemigo.play("die")
	queue_free()
</details>

<p align="center">
  <img src="https://media.tenor.com/bhxZ5O_Xnq8AAAAj/page-divider-glittery.gif" />
</p>

<details>
  <summary style="color:#708090;">NPC</summary>
extends CharacterBody2D

# Tipos de NPC mediante enumeración
enum NPC_DType {barbon, morro, señora, viejo}

# Propiedades configurables
@export var velocidad := 60
@export var gravedad := 1000
@export var patrulla := 30
@export var daño := 1
@export var type: NPC_DType = NPC_DType.barbon

# Referencia al sprite
@onready var sprite_npc = $spritenpc

# Variables de movimiento
var direction := -1
var start_position := Vector2.ZERO

func _ready():
	start_position = global_position
	ActuNPC()  # Configuración inicial según tipo
	collision_layer = 1
	collision_mask = 1

func _physics_process(delta):
	# Movimiento básico similar al enemigo
	velocity.x = direction * velocidad

	if not is_on_floor():
		velocity.y += gravedad * delta
	else:
		velocity.y = 0

	move_and_slide()

	# Lógica de patrulla
	if abs(global_position.x - start_position.x) > patrulla:
		direction *= -1
		sprite_npc.flip_h = direction < 0

func ActuNPC():
	"""
	Configura propiedades específicas para cada tipo de NPC.
	"""
	match type:
		NPC_DType.barbon:
			sprite_npc.play("barbon_mov")
			velocidad = 40
		NPC_DType.morro:
			sprite_npc.play("hatman_mov")
			velocidad = 90 
		NPC_DType.señora:
			sprite_npc.play("woman_mov")
			patrulla = 30
		NPC_DType.viejo:
			sprite_npc.play("olman_mov")
			patrulla = 20
			velocidad = 20
</details>

<details>
  <summary style="color:#708090;">Agua</summary>
extends Area2D

# Tipos de plataforma líquida
enum AguaType {verde, rojo}

# Tipo configurable
@export var type: AguaType = AguaType.verde

func _ready():
	ActuPlat()  # Configuración inicial
	monitorable = true
	monitoring = true

func ActuPlat():
	"""
	Configura las propiedades visuales y movimiento según el tipo.
	"""
	match type:
		AguaType.verde:
			modulate.a = 0.7  # Transparencia
			AGUA_MOV()  # Inicia animación de movimiento
		AguaType.rojo:
			modulate.a = 0.9
			$TileMapLayer.modulate = Color.RED
			LAVA_MOV()  # Inicia animación de movimiento

func AGUA_MOV():
	"""
	Animación de movimiento para agua usando tweens.
	Movimiento suave en bucle.
	"""
	var tween = create_tween()
	tween.tween_property(self, "position:x", position.x +10, .5)
	tween.tween_property(self, "position:y", position.y +2, .2)
	tween.tween_property(self, "position:x", position.x -10, .5)
	tween.tween_property(self, "position:y", position.y -2, .2)
	tween.set_loops()  # Animación en bucle infinito

func LAVA_MOV():
	"""
	Animación de movimiento para lava (más lenta que el agua).
	"""
	var tween = create_tween()
	tween.tween_property(self, "position:x", position.x +10, 1.5)
	tween.tween_property(self, "position:y", position.y +2, .2)
	tween.tween_property(self, "position:x", position.x -10, 1.5)
	tween.tween_property(self, "position:y", position.y -2, .2)
	tween.set_loops()  # Animación en bucle infinito
</details>

<h1></h1>

<details>
	""
	animacion y funcion para activar el ataque del personaje hacia los enemigos 
	""
	func atacar():
	atacando = true
	$AttackArea.monitoring = true  # activa la detección de colisión
	sprite.play("ataque")  # la animación debe llamarse "ataque"

	await get_tree().create_timer(0.3).timeout  # tiempo activo de ataque
	$AttackArea.monitoring = false
	atacando = false
</details>
<h1></h1>

<details>
	"" sistema de guardado
	""
	# Variables ya existentes
var vidas = 3
var monedas = 0

# GUARDADO
func guardar_datos():
	var save_data = {
		"posicion": global_position,
		"vidas": vidas,
		"monedas": monedas
	}
	var file = FileAccess.open("user://jugador.save", FileAccess.WRITE)
	file.store_var(save_data)
	file.close()

func cargar_datos():
	if FileAccess.file_exists("user://jugador.save"):
		var file = FileAccess.open("user://jugador.save", FileAccess.READ)
		var save_data = file.get_var()
		file.close()

		if "posicion" in save_data:
			global_position = save_data["posicion"]
		if "vidas" in save_data:
			vidas = save_data["vidas"]
		if "monedas" in save_data:
			monedas = save_data["monedas"]
			label_monedas.text = str(monedas)

		AnimVidas()  # para que se actualicen las imágenes de vida

# Llamar al cargar escena
func _ready():
	# ...
	cargar_datos()

# Detectar tecla de guardado
func _input(event):
	if event.is_action_pressed("guardar"):
		guardar_datos()

  </details>
  <h1></h1>
<h1 align="center" style="font-weight:bold; color:#708090;">Dificultades</h1>

<div align="center">
  <p><strong>maria</strong> he de confesar que este juego lo recolecte del juego anterior que hice con mi compañero y mi gran amigo abdiel, el cual tuve en mente agregarle el modo ataque, el modo guardado y la mejora del segundo nivel.</p>
  <p>solo tuve un pequeño problema y es el que a mi no se me da el decorar de lo mejor, puedo confesar que me la pase mas horas diseñando que programando.</p>
  
</div>

<h1></h1>
<h1 align="center" style="font-weight:bold; color:#708090;">Conclusión</h1>
En conclusion, es un juego en el cual pude hacercarme mas al mundo del videojuego, ya que yo no suelo ser de jugar videojuegos y esto me abrio el panorama, al igual de reforzar mi uso de godot y la logica de programcion que se empleo.

<p></p>
<p></p>

<p align="center">
  <img src="https://media1.tenor.com/m/bmxrC5x1kX8AAAAd/taykumix-divider.gif" />
</p>
