# Wall-area-problem
using constructors we calculate a wall area 

public class Wall {

    private double height;
    private double width;

    public Wall(double width, double height) {
        this.height = height < 0? 0: height;
        this.width = width < 0 ? 0: width;
    }

    public Wall() {
    }

    public double getHeight() {
        return this.height;
    }

    public double getWidth() {
        return this.width;
    }

    public double getArea(){
        if(this.width < 0 || this.height < 0){
            this.width = 0; this.height = 0;
        }
        return this.width * this.height;
    }

    public void setHeight(double height) {
        if(height < 0){
            this.height = 0;
        } else {
            this.height = height;
        }
    }

    public void setWidth(double width) {
        if(width < 0){
            this.width = 0;
        } else {
            this.width = width;
        }
    }
    
    
    public static void main(String[] args){
    
    Wall wall = new Wall(1.25, 21.25);
    System.out.println("area= " + wall.getArea());
    System.out.println();
    System.out.println("width= " + wall.getWidth());
    wall.setHeight(1.4);
    System.out.println("height= " + wall.getHeight());
    System.out.println("Area= " + wall.getArea());
    }
}


