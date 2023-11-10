#include <stdio.h>
#include <stdlib.h>
#include <time.h>

enum EXITSTATUS{ OK=0, FILE_READ_ERROR, NO_FILE_SPECIFIED };
int n=0;

double* getValues(const char* fileName){
	FILE* file = fopen(fileName, "r");
	if(file == NULL){
		printf("couldnt open file : %s\n",fileName);
		return NULL;
	}	
	
	n = 0;
	double value = 0;
	while(fscanf(file, "%lf", &value) == 1)
		++n;
	double* array = NULL;
	if(n > 0){
		rewind(file);
		array = malloc(n * sizeof(double));
		if(array == NULL){
			fclose(file);
			return NULL;
		}
		int i = 0;
		while(fscanf(file, "%lf", &array[i]) == 1)
			++i;
	}

	return array;
}


void sort(double* array){
	MergeSort(array, 0, n-1);
}

void MergeSort(double* array, const int begin, const int end){
	if(begin >=end) return;

	int mid = begin+(end-begin)/2;
	MergeSort(array,begin,mid);
	MergeSort(array,mid + 1, end);
	merge(array,begin,mid,end);

}

void merge(double* array, const int left, const int mid, const int right){
    const int subArrayOne = mid - left + 1;
    const int subArrayTwo = right - mid;
 
    // Create temp arrays
    double *leftArray = malloc(subArrayOne * sizeof(double)),
         *rightArray =  malloc(subArrayTwo * sizeof(double));
 
    // Copy data to temp arrays leftArray[] and rightArray[]
    for (auto i = 0; i < subArrayOne; ++i)
        leftArray[i] = array[left + i];
    for (auto j = 0; j < subArrayTwo; ++j)
        rightArray[j] = array[mid + 1 + j];
 
    int indexOfSubArrayOne = 0, indexOfSubArrayTwo = 0;
    int indexOfMergedArray = left;
 
    // Merge the temp arrays back into array[left..right]
    while (indexOfSubArrayOne < subArrayOne
           && indexOfSubArrayTwo < subArrayTwo) {
        if (leftArray[indexOfSubArrayOne]
            <= rightArray[indexOfSubArrayTwo]) {
            array[indexOfMergedArray]
                = leftArray[indexOfSubArrayOne];
            indexOfSubArrayOne++;
        }
        else {
            array[indexOfMergedArray]
                = rightArray[indexOfSubArrayTwo];
            indexOfSubArrayTwo++;
        }
        indexOfMergedArray++;
    }
 
    // Copy the remaining elements of
    // left[], if there are any
    while (indexOfSubArrayOne < subArrayOne) {
        array[indexOfMergedArray]
            = leftArray[indexOfSubArrayOne];
        indexOfSubArrayOne++;
        indexOfMergedArray++;
    }
 
    // Copy the remaining elements of
    // right[], if there are any
    while (indexOfSubArrayTwo < subArrayTwo) {
        array[indexOfMergedArray]
            = rightArray[indexOfSubArrayTwo];
        indexOfSubArrayTwo++;
        indexOfMergedArray++;
    }
    free(leftArray);
    free(rightArray);

}


void printArray(const double* array){
	for(int i=0;
	    i<n;
	    ++i)
		printf("%lf\n",array[i]);
	printf("\n");
}

int main(int argc, char** argv){
	if(argc < 2){
		printf("you didn`t pass file to sort\n");
		return NO_FILE_SPECIFIED;
	}
		
	char* filePath = argv[1];
	double *array = getValues(filePath);
	printf("opening file %s", filePath);
	if(array == NULL){
		printf("couldnt open file : %s/n", filePath);
		return FILE_READ_ERROR;
	}

	sort(array);

	//printArray(array);
	
	free(array);
	return OK;
}
