public Learner(String rollNo, String fullName) {
    this.rollNo = rollNo;
    this.fullName = fullName;
    this.scores = new ArrayList<>();
}

public void addScore(int score) {
    scores.add(score);
}

public double calculateAverage() {
    if (scores.isEmpty()) return 0.0;
    int total = 0;
    for (int s : scores) total += s;
    return (double) total / scores.size();
}

public int getMaxScore() {
    if (scores.isEmpty()) return 0;
    return Collections.max(scores);
}

public int getMinScore() {
    if (scores.isEmpty()) return 0;
    return Collections.min(scores);
}

@Override
public String toString() {
    return "Roll No: " + rollNo + ", Name: " + fullName +
           ", Scores: " + scores +
           ", Average: " + String.format("%.2f", calculateAverage()) +
           ", Highest: " + getMaxScore() +
           ", Lowest: " + getMinScore();
}# main.java

