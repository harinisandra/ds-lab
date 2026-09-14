class Node:
	def __init__(self, data):
		self.data = data
		self.previous = None
		self.next = None


class InsertStart:
	def __init__(self):
		self.head = None
		self.tail = None

	def addAtStart(self, data):
		new_node = Node(data)
		if self.head is None:
			self.head = self.tail = new_node
			return

		new_node.next = self.head
		self.head.previous = new_node
		self.head = new_node

	def display(self):
		if self.head is None:
			print("List is empty")
			return

		current = self.head
		print("Adding a node to the start of the list:")
		while current is not None:
			print(current.data, end=" ")
			current = current.next
		print()


if __name__ == "__main__":
	d_list = InsertStart()
	for value in range(1, 6):
		d_list.addAtStart(value)
		d_list.display()
