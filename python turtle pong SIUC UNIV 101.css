

import turtle

#screen
wn = turtle.Screen()
wn.title("Pong by Univ101 - SIUC")
wn.bgcolor("maroon")
wn.setup (width=1000, height=500)
wn.tracer(0)


# Paddle A 
paddle1y = 0
paddle_a = turtle.Turtle()
paddle_a.speed(0)
paddle_a.shape("square")
paddle_a.color("white")
paddle_a.shapesize(stretch_wid=5, stretch_len=0.5)
paddle_a.penup()
paddle_a.goto(-450, 0)
# Paddle B 
paddle2y = 0
paddle_b = turtle.Turtle()
paddle_b.speed(0)
paddle_b.shape("square")
paddle_b.color("black")
paddle_b.shapesize(stretch_wid=5, stretch_len=0.5)
paddle_b.penup()
paddle_b.goto(450, 0)
# Ball
ball = turtle.Turtle()
ball.speed(0)
ball.shape("circle")
ball.color("yellow")
ball.shapesize(stretch_wid=1, stretch_len=1)
ball.penup()
ball.goto(0, 0)
ball.dx = 0.1
ball.dy = 0.1
# SCORE
score = turtle.Turtle()
score.speed(0)
score.color: ("black")
score.penup()
score.hideturtle()
score.write("White : 0   Black : 0", align="center", font=("Courier",30,"normal"))


score_w = 0
score_b = 0

#Function
def paddle_b_up():
	y = paddle_b.ycor()
	if y <200:
		y += 40
		paddle_b.sety(y)

def paddle_b_down():
	y = paddle_b.ycor()
	if y >-200:
		y -= 80
		paddle_b.sety(y)
def paddle_a_up():
	y = paddle_a.ycor()
	if y <200:
		y += 40
		paddle_a.sety(y)

def paddle_a_down():
	y = paddle_a.ycor()
	if y >-200:
		y -= 80
		paddle_a.sety(y)
	



		


#Keyboard binding
wn.listen()
wn.onkeypress(paddle_a_up, "w")
wn.listen()
wn.onkeypress(paddle_a_down, "s")

wn.listen()
wn.onkeypress(paddle_b_up, "Up")
wn.listen()
wn.onkeypress(paddle_b_down, "Down")

while True:
	wn.update()

	#move ball
	ball.setx(ball.xcor() + ball.dx)
	ball.sety(ball.ycor() + ball.dy)
	#border check
	#top check

	if ball.ycor() > 250:
		ball.sety(250)
		ball.dy *=-1
	if ball.ycor() < -250:
		ball.sety(-250)
		ball.dy *=-1
	#side checks
	#right
	if ball.xcor() > 500:
		ball.setx(500)
		ball.goto(0,0)
		ball.dx = 0.08
		ball.dx *=-1
		score_w +=1
		score.clear()
		score.write("White: {}   Black: {}".format(score_w, score_b), align="center", font=("Courier",30,"normal"))
	#left
	if ball.xcor() < -500:
		ball.goto(0,0)
		ball.dx = 0.08
		ball.dx *=-1
		score_b +=1	
		score.clear()
		score.write("White: {}   Black: {}".format(score_w, score_b), align="center", font=("Courier",30,"normal"))
	#COLLISION CHECK
	if (ball.xcor() > 440 and (ball.xcor()<450)) and (ball.ycor() < paddle_b.ycor() + 80 and ball.ycor() > paddle_b.ycor() - 80 ):
		ball.dx *= -1.1

	if (ball.xcor() < -440 and (ball.xcor()>-450)) and (ball.ycor() < paddle_a.ycor() + 80 and ball.ycor() > paddle_a.ycor() - 80 ):
		ball.dx *= -1.1