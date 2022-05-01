# K3MD
//code starts from here
int t, n, d, arr[], sum;
		Scanner sc = new Scanner(System.in);
	    t = sc.nextInt();
	    
	    while(t-- > 0) {
	        sum = 0;
	        n = sc.nextInt();
	        d = sc.nextInt();
	        arr = new int[d];
	        // input arr
	        for(int i = 0; i < d; i++) {
	            arr[i] = sc.nextInt();
	            sum += arr[i];
	        }
	        
	        n = n%sum;
	        if(n == 0) {
	            System.out.println(d);
	        } 
	        else {
    	        // count the day
    	        for(int day = 1; day <= d; day++) {
    	            n -= arr[day-1];
    	            if(n <= 0) {
    	                System.out.println(day);
    	                break;
    	            }
    	            if(day == d)
    	                day = 0;    // make day = 0, so that day++ makes it 1
    	        }
	        }
	    }
