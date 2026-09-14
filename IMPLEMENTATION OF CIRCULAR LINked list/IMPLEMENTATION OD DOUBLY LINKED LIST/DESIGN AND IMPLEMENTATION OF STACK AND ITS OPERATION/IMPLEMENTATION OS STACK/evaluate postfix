class Evaluate:
    def __init__(self, capacity):
        self.top = -1
        self.capacity = capacity
        self.array = []

    def isEmpty(self):
        return self.top == -1

    def peek(self):
        if self.isEmpty():
            raise ValueError("Stack is empty")
        return self.array[-1]

    def pop(self):
        if self.isEmpty():
            raise ValueError("Invalid postfix expression")
        self.top -= 1
        return self.array.pop()

    def push(self, value):
        self.top += 1
        self.array.append(value)

    def evaluatePostfix(self, expression):
        for character in expression:
            if character.isspace():
                continue

            if character.isdigit():
                self.push(int(character))
                continue

            right = self.pop()
            left = self.pop()
            if character == "+":
                result = left + right
            elif character == "-":
                result = left - right
            elif character == "*":
                result = left * right
            elif character == "/":
                if right == 0:
                    raise ZeroDivisionError("division by zero")
                result = left // right
            else:
                raise ValueError(f"Unsupported operator: {character}")
            self.push(result)

        if len(self.array) != 1:
            raise ValueError("Invalid postfix expression")
        return self.pop()


if __name__ == "__main__":
    expression = "231*+9-"
    evaluator = Evaluate(len(expression))
    print("Postfix evaluation:", evaluator.evaluatePostfix(expression))
