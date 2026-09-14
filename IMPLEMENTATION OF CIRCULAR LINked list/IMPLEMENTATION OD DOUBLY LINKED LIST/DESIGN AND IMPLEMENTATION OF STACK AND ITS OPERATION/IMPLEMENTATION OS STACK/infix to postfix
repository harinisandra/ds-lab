class Conversion:
	def __init__(self, capacity):
		self.top = -1
		self.capacity = capacity
		self.array = []
		self.precedence = {"+": 1, "-": 1, "*": 2, "/": 2, "^": 3}

	def isEmpty(self):
		return self.top == -1

	def peek(self):
		return self.array[-1]

	def pop(self):
		if self.isEmpty():
			return "$"
		self.top -= 1
		return self.array.pop()

	def push(self, operator):
		self.top += 1
		self.array.append(operator)

	def isOperand(self, character):
		return character.isalnum()

	def notGreater(self, operator):
		if self.peek() == "(":
			return False
		return self.precedence[operator] <= self.precedence[self.peek()]

	def infixToPostfix(self, expression):
		output = []
		for character in expression:
			if character.isspace():
				continue

			if self.isOperand(character):
				output.append(character)
			elif character == "(":
				self.push(character)
			elif character == ")":
				while not self.isEmpty() and self.peek() != "(":
					output.append(self.pop())
				if self.isEmpty():
					raise ValueError("Mismatched parentheses")
				self.pop()
			else:
				while not self.isEmpty() and self.notGreater(character):
					output.append(self.pop())
				self.push(character)

		while not self.isEmpty():
			if self.peek() == "(":
				raise ValueError("Mismatched parentheses")
			output.append(self.pop())

		return "".join(output)


if __name__ == "__main__":
	expression = "a+b*(c^d-e)^(f+g*h)-i"
	converter = Conversion(len(expression))
	print(converter.infixToPostfix(expression))
