class Node:
	def __init__(self, data):
		self.data = data
		self.next = None


class Stack:
	def __init__(self):
		self.head = None

	def isempty(self):
		return self.head is None

	def push(self, data):
		new_node = Node(data)
		new_node.next = self.head
		self.head = new_node

	def pop(self):
		if self.isempty():
			return None

		popped_node = self.head
		self.head = self.head.next
		popped_node.next = None
		return popped_node.data

	def peek(self):
		if self.isempty():
			return None
		return self.head.data

	def display(self):
		if self.isempty():
			print("Stack Underflow")
			return

		current = self.head
		while current is not None:
			print(current.data, "->", end=" ")
			current = current.next
		print()


if __name__ == "__main__":
	my_stack = Stack()
	my_stack.push(11)
	my_stack.push(22)
	my_stack.push(33)
	my_stack.push(44)

	my_stack.display()
	print("\nTop element is", my_stack.peek())

	my_stack.pop()
	my_stack.pop()
	my_stack.display()
	print("\nTop element is", my_stack.peek())
