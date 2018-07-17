# hello-wxx
just a simple project


import java.util.ArrayList;
import java.util.LinkedList;
import java.util.Queue;

public class Solution {
	public void printBinaryTreeByFloor(TreeNode root){
		if(root == null){
			return;
		}
		int floor = 1;
		Queue<TreeNode> queue = new LinkedList<TreeNode>();
		queue.add(root);
		while(!queue.isEmpty()){
			int size = queue.size();
			for(int i=0;i<size;i++){
				TreeNode node = queue.poll();
				System.out.print(node.getVal());
				if(node.getLeft() != null){
					queue.add(node.getLeft());
				}
				if(node.getRight() != null){
					queue.add(node.getRight());
				}
			}
			System.out.println();
		}
	}
}
