# Ap-Prep
public class ArrayUtil {

	/**
	 * Reverse elements of array arr Precondition: arr.length > 0. Postcondition:
	 * The elements of arr have been reversed
	 * 
	 * @param arr
	 *            the array to manipulate
	 */
	public static void reverseArray(int[] arr) {
		/* code goes here */
		int[] newArray = new int[arr.length];
		int counter = 0;
		for (int i = arr.length; i < arr.length - 1; i--) {
			newArray[counter] = arr[i];
			counter++;
		}

		for (int l = 0; l < arr.length - 1; l++) {
			System.out.println(newArray[l]);
		}
	}

	public static void main(String[] args) {
		int[][] testArr = { { 12, 11, 10, 9 }, { 8, 7, 6, 5 }, { 4, 3, 2, 1 } };
		int[] testArr2 = { 12, 11, 10, 9 };
		Matrix m = new Matrix(testArr);
		m.reverseAllRows();

	}
}

class Matrix {
	private int[][] mat;

	public Matrix(int[][] m) {
		mat = m;
	}

	/**
	 * Revereses the elements in each row of mat. Postcondition: The elements in
	 * each row have been reversed
	 */
	public void reverseAllRows() {

		System.out.println(mat);
		int[][] newMat = new int[mat.length][];
		int counter = 0;
		for (int i = 0; i < mat.length - 1; i++) {
			int[] newArray = new int[mat[i].length];
			for (int j = mat.length; j < mat.length - 1; j--) {
				newArray[counter] = mat[i][j];
				counter++;

			}

			newMat[i] = newArray;

			counter = 0;

		}

		for (int l = 0; l < newMat.length - 1; l++) {
			for (int m = 0; m < newMat[l].length - 1; m++)
				System.out.println(newMat[l][m]);
		}
		System.out.println(" ");
		System.out.println(newMat);

	}

	/**
	 * Reverses the elements of mat. Postcondition: - The final elements of mat,
	 * when read in row-major order, are the same as the original elements of mat
	 * when read from the bottom corner, right to left, going upward. - mat[0][0]
	 * contains what was originally the last element. - mat[mat.length -
	 * 1][mat[0].length -1] contains what was originally the first element.
	 */
	public void reverseMatrix() {

	}

	public int[][] getIntArray() {
		return mat;
	}
}
