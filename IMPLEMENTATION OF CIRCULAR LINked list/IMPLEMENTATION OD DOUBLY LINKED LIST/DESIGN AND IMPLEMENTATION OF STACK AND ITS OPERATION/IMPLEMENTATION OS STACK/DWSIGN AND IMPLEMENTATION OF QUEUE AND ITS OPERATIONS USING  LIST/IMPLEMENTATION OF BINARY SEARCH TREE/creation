class Node:
	def __init__(self, key):
		self.data = key
		self.left = None
		self.right = None


def insert(node, data):
	if node is None:
		return Node(data)

	if data <= node.data:
		node.left = insert(node.left, data)
	else:
		node.right = insert(node.right, data)
	return node


def minValue(node):
	current = node
	while current.left is not None:
		current = current.left
	return current.data


if __name__ == "__main__":
	root = None
	for value in (4, 2, 1, 3, 6, 5):
		root = insert(root, value)

	print("\nMinimum value in BST is %d" % minValue(root))
